<template>
  <div class="ergonomics">
    <div class="table">
      <img class="table__img table-top" src="@/img/table-top.png" alt="Столешница" />
      <div class="table-buttons">
        <button type="button" class="table-buttons__item button-top" @click="raise">вверх</button>
        <button type="button" class="table-buttons__item button-bottom" @click="lower">вниз</button>
      </div>
      <img class="table__img table-bottom top-400" src="@/img/table-bottom.png" alt="Ножки стола" />
    </div>
    <div class="description">
      <h1 class="headline blue">Эргономика — ключ к успеху совеременного человека</h1>
      <p class="text near-black">Cтильная столешница , выполненной из экологически безопасного материала (ДСП), и усиленной стальной рамы не
        составит труда разместить на поверхности инновационного стола большое количество крупногабаритной техники: стол
        выдерживает нагрузку до 80 кг.
      </p>
      <p class="text near-black">Также столешница, обладающая меламиновым покрытием, хорошо переносит механические
        воздействия (царапины или удары), при контакте с водой не разрушается, устойчиво переносит бытовые химические
        вещества и не выгорает под воздействием ультрафиолета.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',

  methods: {
    raise: function () {
      let tableBottom = document.querySelector(".table-bottom");
      if (tableBottom.classList.contains("top-450")) {
        tableBottom.classList.remove("top-450");
        tableBottom.classList.add("top-500");
      }
      if (tableBottom.classList.contains("top-400")) {
        tableBottom.classList.remove("top-400");
        tableBottom.classList.add("top-450");
      }
      if (tableBottom.classList.contains("top-350")) {
        tableBottom.classList.remove("top-350");
        tableBottom.classList.add("top-400");
      }
      if (tableBottom.classList.contains("top-300")) {
        tableBottom.classList.remove("top-300");
        tableBottom.classList.add("top-350");
      }
      if (tableBottom.classList.contains("top-250")) {
        tableBottom.classList.remove("top-250");
        tableBottom.classList.add("top-300");
      }
    },

    lower: function () {
      let tableBottom = document.querySelector(".table-bottom");
      if (tableBottom.classList.contains("top-300")) {
        tableBottom.classList.remove("top-300");
        tableBottom.classList.add("top-250");
      }
      if (tableBottom.classList.contains("top-350")) {
        tableBottom.classList.remove("top-350");
        tableBottom.classList.add("top-300");
      }
      if (tableBottom.classList.contains("top-400")) {
        tableBottom.classList.remove("top-400");
        tableBottom.classList.add("top-350");
      }
      if (tableBottom.classList.contains("top-450")) {
        tableBottom.classList.remove("top-450");
        tableBottom.classList.add("top-400");
      }
      if (tableBottom.classList.contains("top-500")) {
        tableBottom.classList.remove("top-500");
        tableBottom.classList.add("top-450");
      }
    },
  }
}
</script>
