<template>
  <div class="home">
  <header  id="head">
    <h1>Защити свои данные</h1>
    <div id="sign-log">
      <button @click="main_log_open = true, main_reg_open = false" >Войти</button>
      <button @click="main_reg_open = true, main_log_open = false">Регистрация</button>
    </div>
    <div hidden id="name">
      <h2>{{name}} {{lastname}}</h2>
    </div>
  </header>


  <main>
    <div id='forma'>
      <textarea></textarea>
      <button >Кодировать</button>
    </div>

    <div id="mod_menu">
      <div hidden  id="user">
        <button @click="main_reg_open = false, main_log_open = false">Выход</button>
      </div>

      <form method="post" :class="{hiddendiv: !main_reg_open}" class="menu" id="reg">
        <input type="text" name="name" required placeholder="Введите Имя">
        <input type="text" name="lastname" required  placeholder="Введите Фамилию">
        <input type="text" name="login" required  placeholder="Введите логин">
        <input type="password" name="password" required  placeholder="Введите пароль">
        <button >Регистрация</button>
      </form>

      <form method="post" :class="{hiddendiv: !main_log_open}" class="menu" id="log">
        <input type="text" name="login" required  placeholder="Введите логин">
        <input type="password" name="password" required  placeholder="Введите пароль">
        <button >Войти</button>
      </form>

    </div>
  </main>
  </div>
</template>

<script>


export default {
  name: 'Home',
  data: () =>({
    main_reg_open: false,
    main_log_open: false,
  })
}
</script>
