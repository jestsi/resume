<template>
  <q-page>
    <q-container>
      <q-row justify="center">
        <q-col>
          <q-btn-group unelevated class="floating-nav">
            <q-btn
              class="floating-nav-btn"
              v-for="option in options"
              flat
              :key="option.value"
              @click="goToText(option.value)"
              >{{ option.label }}</q-btn
            >
          </q-btn-group>
        </q-col>
      </q-row>
    </q-container>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      tab: 'Work',
      options: [
        { label: 'Главная', value: 'main' },
        { label: 'Навыки', value: 'skills' },
        { label: 'Контакты', value: 'contact' },
      ],
      showFloatingNavBar: true,
    };
  },
  methods: {
    goToText(id) {
      const element = document.getElementById(id);
      if (element) element.scrollIntoView({ behavior: 'smooth' });
    },
    checkScrollPosition(event) {
      const scrollTop = window.scrollY || document.documentElement.scrollTop;
      const triggerHeight = 300; // Высота, на которой нужно скрыть панель

      if (scrollTop < triggerHeight) {
        this.showFloatingNavBar = false;
      } else {
        this.showFloatingNavBar = true;
      }
    },
  },
  watch: {
    showFloatingNavBar(newValue) {
      const floatingNav = this.$el.querySelector('.floating-nav');
      if (newValue) {
        floatingNav.classList.remove('hide');
      } else {
        floatingNav.classList.add('hide');
      }
    },
  },
  mounted() {
    window.addEventListener('scroll', this.checkScrollPosition);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.checkScrollPosition);
  },
};
</script>

<style scoped lang="scss">
$floating-nav-bg: rgba($primary, 0.7);

.floating-nav {
  position: fixed;
  bottom: 90vh;
  transform: translateX(-50%);
  background: $floating-nav-bg;
  border-radius: 20px;
  color: #fff;
  padding-top: 4px;
  padding-bottom: 4px;
  align-content: center;
  transition: opacity 0.3s ease, transform 0.3s ease;
  opacity: 1;
  pointer-events: all;
}

.floating-nav.hide {
  opacity: 0;
  transform: translateX(-50%) translateY(-20px);
  pointer-events: none;
}
</style>
