<script lang="ts">
import UserIcon from '@/assets/user-solid.svg';
import LockIcon from '@/assets/lock-solid.svg';
import axios from 'axios';

export default {
  data() {
    return {
      userIcon: UserIcon,
      lockIcon: LockIcon,
      username: '',
      password: '',
    };
  },
  methods: {
    loginHandler(event: any) {
      console.log({ ...event });
      axios
        .post('http://localhost:3000/users', {
          username: this.username,
          password: this.password,
        })
        .then((response) => {
          console.log({ ...response });
        });
    },
  },
};
</script>

<template>
  <div id="page-login">
    <div id="page-login-cover">
      <div id="page-cover-text">Welcome Back.</div>
    </div>
    <div id="page-login-form">
      <div id="page-form-label">Login to an existing account</div>
      <div class="page-form-input">
        <img class="form-icon" :src="userIcon" alt="e-mail" />
        <input
          type="tel"
          placeholder="e-mail"
          name="user-name"
          id="input-user-name"
          v-model="username"
        />
      </div>
      <div class="page-form-input">
        <img class="form-icon" :src="lockIcon" alt="" />
        <input
          type="password"
          placeholder="password"
          name="user-password"
          id="input-user-password"
          v-model="password"
        />
      </div>
      <div id="page-form-button">
        <button @click="loginHandler">Log in</button>
      </div>
    </div>
  </div>
</template>

<style>
:root {
  --size-line-height: 8vw;
  --size-form-icon: 20px;
}

div#page-login {
  display: flex;
  margin-top: -20px;
  height: calc(100vh - 60px);
}

div#login-page > * {
  height: 100%;
}

div#page-login-cover {
  background-color: #5e5eff;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: end;
}

div#page-cover-text {
  margin-bottom: 10vh;
  margin-left: 5vh;
  font-size: var(--size-line-height);
  line-height: var(--size-line-height);
  font-weight: bold;
  color: white;
}

div#page-login-form {
  width: 50%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

div#page-form-label {
  font-weight: bold;
  margin: 40px 0;
}

div.page-form-input {
  display: flex;
  align-items: center;
  background-color: #ddd;
  padding: 15px;
  border-radius: 40px;
  margin-bottom: 20px;
  width: 70%;
}

div.page-form-input input {
  margin-left: 20px;
  border: none;
  outline: none;
  background: none;
}

img.form-icon {
  height: var(--size-form-icon);
}

div#page-form-button {
  width: 70%;
}

div#page-form-button button {
  width: 100%;
  background-color: grey;
  color: white;
  font-weight: bold;
  height: 40px;
  border: none;
  outline: none;
  border-radius: 5px;
  cursor: grab;
}
</style>
