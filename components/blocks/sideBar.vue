<template>
  <div class="sidebar">
    <span class="arrow"></span>
    <Logo width='80' class="mb-12 sm:mb-9" />
    <nav>
      <ul
        v-for="(item, i) in menu"
        :key="i"
      >
        <li class="sidebar__item flex mb-6">
          <img :src="item.src" alt="">
          <NuxtLink :to="item.to" class="ml-2 w-full">{{item.name}}</NuxtLink>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
import Logo from '@/components/icons/logo'

export default {
  components: {
    Logo
  },
  data () {
    return {
      menu: [
        {
          name: 'Мой профиль',
          to: '/profile',
          src: require('@/assets/images/todo.svg')
        },
        {
          name: 'Список задач',
          to: '/todos',
          src: require('@/assets/images/todo.svg')
        },
        {
          name: 'Статистика',
          to: '/statistics',
          src: require('@/assets/images/todo.svg')
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.sidebar {
  position: relative;
  padding: 24px 0px 48px 56px;
  width: 300px;

  &__item {
    font-family: Montserrat;
    font-size: 14px;
    font-weight: 500;

    &:hover {
      color: #BD0D22;
    }
  }
}

.arrow {
  position: absolute;
  right: -20px;
  top: 20px;
  box-shadow: 0px 1px 2px rgba(0, 0, 0, 0.15);
  box-sizing: border-box;
  background: #fff;
  display: block;
  transform: scale(var(--ggs,1));
  width: 40px;
  height: 40px;
  border: 2px solid transparent;
  border-radius: 100px;
  cursor: pointer;
}
.arrow::after {
  content: "";
  display: block;
  box-sizing: border-box;
  position: absolute;
  width: 2px;
  height: 14px;
  border-left: 2px solid #6FBC9A;
  top: 2px;
  left: 0
}
.arrow::after {
  width: 10px;
  height: 10px;
  border-bottom: 2px solid #6FBC9A;
  transform: rotate(45deg);
  left: 15px;
  top: 14px
}

</style>
