<template>
  <div class="auth">

    <my-button class="auth__login" variant="secondary">Log in</my-button>
    <div class="auth__section auth__section--left">
      <Logo/>
    </div>

    <div class="auth__section auth__section--right">
      <form class="auth__form">
        <h1 class="auth__title">Create an account</h1>
        <p class="auth__text">Enter your email below to create your account</p>

        <div class="auth__controls">
          <Input class="auth__input" type="email" placeholder="Email" />
          <my-button class="auth__submit">Sign In with Email</my-button>
          <my-button class="auth__login" variant="secondary">Log in</my-button>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup>
import Logo from "@/components/Logo.vue";
import { Input } from '@/components/ui/input'
import MyButton from "@/components/ui/button/my-button.vue";

</script>

<style scoped lang="scss">
.auth {
  display: flex;
  height: 100vh;

  &__section {
    width: 50%;
    padding: 40px;

    &--left {
      color: #fff;
      background-color: #18181B;
    }

    &--right {
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }

  &__title {
    margin-bottom: 10px;
  }

  &__text {
    margin-bottom: 10px;
  }

  &__submit {
    width: 100%;
  }

  &__input {
    margin-bottom: 10px;
    outline: none;

    &:hover {
      border-color: black;
    }

    &:focus {
      border-color: black;
    }
  }

  &__login {
    position: absolute;
    top: 40px;
    right: 40px;
  }
}

h1 {
  font-size: 1.5rem;
  font-weight: 600;
  letter-spacing: -.025em;
  text-align: center;
}
</style>
