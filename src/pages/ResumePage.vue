<template>
  <q-page class="q-pa-md">
    <div class="q-gutter-md">
      <div id="main">
        <h1 class="q-ma-0">
          <q-icon name="img:/hello_512.png" /> Привет, я Гуц Максим
        </h1>
        <p>
          Я опытный веб-разработчик с более чем четырехлетним опытом кодинга, из
          которых один год я активно занимаюсь веб-разработкой. В настоящее
          время я работаю в компании ООО "КИБЕР-СОФТ", где участвую в разработке
          CRM системы для клиник, используемой по всей России. Я обладаю
          сильными навыками работы с Vue.js (Quasar) и PHP, а также знаком с
          паттернами и архитектурой кода. Мои сильные стороны включают быстрое
          освоение новых технологий, внимательность к деталям и способность
          эффективно работать в команде.
        </p>
      </div>
      <div id="skills">
        <h2>Навыки</h2>
        <ul>
          <li>
            <strong>Фронтенд</strong>:
            <q-icon
              size="3rem"
              default="PGSQL"
              name="img:/vue-js-seeklogo.svg"
            />
            <q-icon size="3rem" default="PGSQL" name="img:/favicon-dark.svg" />
          </li>
          <li>
            <strong>Бэкенд</strong>:
            <q-icon
              size="3rem"
              default="PHP"
              name="img:https://www.php.net/images/logos/php-logo.svg"
            />
          </li>
          <li>
            <strong>СУБД</strong>:
            <q-icon
              size="3rem"
              default="PGSQL"
              name="img:/postgresql-svgrepo-com.svg"
            />,
            <q-icon
              size="5rem"
              default="MYSQL"
              name="img:/mysql-svgrepo-com.svg"
            />
          </li>
          <li>
            <strong>Паттерны и архитектура кода</strong>: Знание основных
            паттернов проектирования и архитектурных принципов
          </li>
          <li>
            <strong>Разработка CRM систем</strong>: Опыт создания и поддержки
            CRM систем для медицинских учреждений
          </li>
        </ul>
        <h3>Так-же был опыт работы с</h3>
        <ul>
          <li><strong>Языки программирования</strong>: C++, C#, Rust</li>
        </ul>
      </div>
      <div id="contact">
        <h2>Контактная информация</h2>
        <p><strong>Email</strong>: gestjobm@gmail.com</p>
        <p><strong>Телефон</strong>: +7 968 278 2319</p>
      </div>
    </div>
  </q-page>
</template>

<script></script>

<style lang="scss" scoped>
div {
  margin: 5%;
}
h2 {
  color: $primary;
}
p {
  padding: 0px 0px 0px 1%;
  text-indent: 1%;
  font-size: x-large;
}
ul {
  list-style-type: disc;
  font-size: x-large;
  margin-left: 1%;
}
</style>
