<template>
<div>
  <div id="app">
    <div id="nav"
      class="navbar navbar-expand-lg navbar-light bg-light"
      style="background-color: #f59e0b !important"
    >
    </div>
    <router-view/>
  </div>
  <div class="Footer">
      <HFooter></HFooter>
  </div>
</div>
</template>

<script>

import HFooter from 'vue-hacktiv8-footer'

export default {
  components: {
    HFooter
  }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto&display=swap');

:root {
	--dark-color-a: #f48d32;
	--dark-color-b: #f9b64d;
	--light-color: #eeeeee;
	--success-color: #5cb85c;
	--error-color: #d9534f;
}

.Footer {
	position: absolute;
    right: 0;
    bottom: 0;
    left: 0;
    /* padding: 1rem; */
}

* {
	font-family: 'Roboto', sans-serif;
	box-sizing: border-box;
	margin: 0;
	padding: 0;
}

body {
	font-family: 'Roboto', sans-serif !important;
	font-size: 16px;
	background: url(https://images.unsplash.com/photo-1571757767119-68b8dbed8c97?auto=format&fit=crop&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&q=80&w=1350);
	background-repeat: no-repeat;
    background-size: cover;
}

ul {
	list-style: none;
}

a {
	text-decoration: none;
}

.btn {
	cursor: pointer;
	padding: 5px 15px;
	background: var(--light-color);
	color: var(--dark-color-a);
	border: 0;
	font-size: 17px;
}

/* Chat Page */

.chat-container {
	max-width: 1100px;
	background: #fff;
	margin: 30px auto;
	overflow: hidden;
}

.chat-header {
	background: var(--dark-color-a);
	color: #fff;
	border-top-left-radius: 5px;
	border-top-right-radius: 5px;
	padding: 15px;
	display: flex;
	align-items: center;
	justify-content: space-between;
}

.chat-main {
	display: grid;
	grid-template-columns: 1fr 3fr;
  min-height: 60vh;
}

.chat-sidebar {
	background: var(--dark-color-b);
	color: #fff;
	padding: 20px 20px 60px;
	overflow-y: scroll;
}

.chat-sidebar h2 {
	font-size: 20px;
	background: rgba(0, 0, 0, 0.1);
	padding: 10px;
	margin-bottom: 20px;
}

.chat-sidebar h3 {
	margin-bottom: 15px;
}

.chat-sidebar ul li {
	padding: 10px 0;
}

.chat-messages {
	padding: 30px;
	max-height: 500px;
	overflow-y: scroll;
}

.chat-messages .message {
	padding: 10px;
	margin-bottom: 15px;
	background-color: var(--light-color);
	border-radius: 5px;
	overflow-wrap: break-word;
}

.chat-messages .message .meta {
	font-size: 15px;
	font-weight: bold;
	color: var(--dark-color-b);
	opacity: 0.7;
	margin-bottom: 7px;
}

.chat-messages .message .meta span {
	color: #777;
}

.chat-form-container {
	padding: 20px 30px;
	background-color: var(--dark-color-a);
}

.chat-form-container form {
	display: flex;
}

.chat-form-container input[type='text'] {
	font-size: 16px;
	padding: 5px;
	height: 40px;
	flex: 1;
}

/* Join Page */
.join-container {
	max-width: 500px;
	margin: 80px auto;
	color: #fff;
}

.join-header {
	text-align: center;
	padding: 20px;
	background: var(--dark-color-a);
	border-top-left-radius: 5px;
	border-top-right-radius: 5px;
}

.join-main {
	padding: 30px 40px;
	background: var(--dark-color-b);
}

.join-main p {
	margin-bottom: 20px;
}

.join-main .form-control {
	margin-bottom: 20px;
}

.join-main label {
	display: block;
	margin-bottom: 5px;
}

.join-main input[type='text'] {
	font-size: 16px;
	padding: 5px;
	height: 40px;
	width: 100%;
}

.join-main select {
	font-size: 16px;
	padding: 5px;
	height: 40px;
	width: 100%;
}

.join-main .btn {
	margin-top: 20px;
	width: 100%;
}

#nav {
  min-height: 50px;
}

@media (max-width: 700px) {
	.chat-main {
		display: block;
	}

	.chat-sidebar {
		display: none;
	}
}
</style>
