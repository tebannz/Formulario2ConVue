<template>
  <div id="app">
    <form>
      <div>
        <label> Título: </label>
        <input v-model="text" />
      </div>

      <hr />

      <div>
        <label>Emoji: </label>
        <select v-model="emoji">
          <option value="🧑🏻‍💻">🧑🏻‍💻</option>
          <option value="👾">👾</option>
          <option value="👽">👽</option>
          <option value="🤖">🤖</option>
        </select>
      </div>

      <hr />

      <div class="calificacion">
        <label> Apreciación: </label>
        <div>
          <input
            value="Regular"
            type="radio"
            name="calificacion"
            v-model="calificacion"
          />
          <label>Regular</label>
        </div>
        <div>
          <input
            value="Bien"
            type="radio"
            name="calificacion"
            v-model="calificacion"
          />
          <label>Bien</label>
        </div>
        <div>
          <input
            value="Muy"
            type="radio"
            name="calificacion"
            v-model="calificacion"
          />
          <label>Muy bien</label>
        </div>
        <div>
          <input
            value="Increible"
            type="radio"
            name="calificacion"
            v-model="calificacion"
          />
          <label>Increible</label>
        </div>
      </div>

      <hr />

      <div>
        <label>Competencias aprendidas:</label>
        <div class="competencias">
          <div>
            <input
              value="Morfología de un componente"
              type="checkbox"
              name="calificacion"
              v-model="competencias"
            />
            <label>Morfología de un componente </label>
          </div>
          <div>
            <input
              value="Directivas"
              type="checkbox"
              name="calificacion"
              v-model="competencias"
            />
            <label>Directivas</label>
          </div>
          <div>
            <input
              value="One-Way y Two-Way data binding"
              type="checkbox"
              name="calificacion"
              v-model="competencias"
            />
            <label>One-Way y Two-Way data binding </label>
          </div>
          <div>
            <input
              value="Estado"
              type="checkbox"
              name="calificacion"
              v-model="competencias"
            />
            <label>Estado</label>
          </div>
          <div>
            <input
              value="El patrón de diseño MVVM "
              type="checkbox"
              name="calificacion"
              v-model="competencias"
            />
            <label>El patrón de diseño MVVM </label>
          </div>
        </div>
      </div>

      <hr />

      <div class="opinion">
        <label>Opinión: </label>
        <textarea v-model="opinion" id="" rows="4"></textarea>
      </div>
    </form>

    <section>
      <h1>{{ emoji }}</h1>
      <h2>{{ text }}</h2>
      <h3>Y me parece {{ calificacion }}</h3>
      <h4>
        He aprendido:
        <p>{{ competencias }}</p>
      </h4>
      <h5>Mi opinión hasta ahora del framework es:</h5>
      <p>{{ opinion }}</p>
    </section>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      emoji: "🧑🏻‍💻",
      text: "Estoy aprendiendo Vue Js",
      calificacion: "Increible",
      competencias: [
        "Morfología de un componente",
        "One-Way y Two-Way data binding",
        "El patrón de diseño MVVM ",
        "Estado",
        "Directivas",
      ],
      opinion: "Ahora podré desarrollar aplicaciones más cómodamente!!",
    };
  },
};
</script>

<style>
body {
  padding: 10px;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  display: grid;
  gap: 10px;
  grid-template-columns: 300px 1fr;
}

form {
  background: black;
  color: white;
  padding: 30px;
  border-radius: 15px;
  display: flex;
  gap: 10px;
  flex-direction: column;
}

form > div {
  display: flex;
  gap: 10px;
}

form .competencias {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
}

form .competencias div {
  display: flex;
  align-items: flex-start;
  gap: 5px;
}

hr {
  width: 100%;
}

section {
  border: 1px solid;
  border-radius: 15px;
  padding: 0px 30px;
  text-align: center;
}

h1 {
  font-size: 60px;
}
</style>
