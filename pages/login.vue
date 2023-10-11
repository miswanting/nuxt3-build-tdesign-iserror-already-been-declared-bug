<script setup lang="ts">
import { MessagePlugin } from "tdesign-vue-next"

const auth = useOAuth2()

const ui = reactive({
  username: "",
  password: "",
})

onMounted(() => {})

async function tryLogin() {
  const res = await auth.login({
    username: ui.username,
    password: ui.password,
  })
  if (res.ok) {
    await MessagePlugin.success("登录成功")
    navigateTo("/dashboard")
  } else MessagePlugin.warning("登录失败")
}
</script>
<template lang="pug">
TLayout.login
  ClientOnly
    template(#fallback)
      TLoading
    TCard(title="登录")
      template(#actions)
        TLink(@click="navigateTo('/register')") 切换至注册
      TForm(@submit="tryLogin")
        TFormItem(label="电话号码" name="phone")
          TInput(data-cy="username" v-model="ui.username")
        TFormItem(label="密码" name="password")
          TInput(type="password" data-cy="password" v-model="ui.password")
        TFormItem
          TButton(type="submit") 登录
</template>
<style scoped lang="sass">
.login
  height: 100vh
  display: grid
  place-items: center
  background: #000212 radial-gradient(ellipse 80% 100% at 50% -20%,rgba(120,119,198,0.3),hsla(0,0%,100%,0))
</style>
