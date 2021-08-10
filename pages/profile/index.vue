<template>
  <div class="">
    <h1 class="mb-8">Мой профиль</h1>
    <wrapper-block class="flex justify-between flex-wrap">
      <div class="w-1/2 pr-20">
        <Input class="block mb-4 w-full" line name="Имя"/>
        <Input class="block mb-4 w-full" line name="Фамилия"/>
      </div>
      <div class="w-1/2">
        <Input class="block mb-4 w-full" line name="Сменить пароль"/>
        <Input class="block mb-4 w-full" line name="Сменить логин"/>
      </div>
      <Button red name="Регистрация" class="btn-profile"/>
    </wrapper-block>
  </div>
</template>

<script>
import WrapperBlock from '@/components/blocks/wrapperContent'
import Input from '@/components/ui/input'
import Button from '@/components/ui/button'

export default {
  layout: 'rootlayout',
  components: {
    WrapperBlock,
    Input,
    Button
  }
}
</script>

<style lang="scss" scoped>
.btn-profile {
  width: 200px;
  margin-left: auto;
}
</style>
