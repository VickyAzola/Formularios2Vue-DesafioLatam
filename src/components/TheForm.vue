<script>
export default {
  name: 'TheFrom',
  data() {
    return {
      titulo: '',
      emoji: '',
      apreciacion: '',
      competencias: [],
      opinion: ''
    }
  }
}
</script>

<template>
  <div class="container">
    <form>
      <div>
        <label for="titulo">Titulo:</label>
        <input id="titulo" v-model="titulo" />
      </div>

      <hr>

      <div>
        <label>Emoji:</label>
        <select v-model="emoji">
          <option value="😍">😍</option>
          <option value="👨‍💻">👨‍💻</option>
          <option value="🤘">🤘</option>
          <option value="🧨">🧨</option>
        </select>
      </div>

      <hr>

      <div class="list">
        <label>Apreciación:</label>
        <ul>
          <li>
            <input type="radio" name="apreciacion" value="Regular" v-model="apreciacion" />
            Regular
          </li>
          <li>
            <input type="radio" name="apreciacion" value="Bien" v-model="apreciacion"/>
            Bien
          </li>
          <li>
            <input type="radio" name="apreciacion" value="Muy Bien" v-model="apreciacion"/>
            Muy Bien
          </li>
          <li>
            <input type="radio" name="apreciacion" value="Increible" v-model="apreciacion"/>
            Increible
          </li>
        </ul>
      </div>

      <hr>

      <div class="list">
        <label>Competencias Aprendidas:</label>
        <ul>
          <li>
            <input type="checkbox" name="competencias" value="Metodología de un componente" v-model="competencias" />
            Metodología de un componente
          </li>
          <li>
            <input type="checkbox" name="competencias" value="Directivas" v-model="competencias"/>
            Directivas
          </li>
          <li>
            <input type="checkbox" name="competencias" value="One-Way y Two-Way data binding" v-model="competencias"/>
            One-Way y Two-Way data binding
          </li>
          <li>
            <input type="checkbox" name="competencias" value="Estado" v-model="competencias"/>
            Estado
          </li>
          <li>
            <input type="checkbox" name="competencias" value="El patrón de diseño MVVM" v-model="competencias"/>
            El patrón de diseño MVVM
          </li>
        </ul>
      </div>

      <hr>

      <div class="opinion">
        <label>Opinión:</label>
        <textarea v-model="opinion"></textarea>
      </div>
    </form>

    <section>
      <p>{{ emoji }}</p>
      <h1>{{ titulo }}</h1>
      <p>Y me parece {{ apreciacion }}</p>
      <p>He Aprendido:</p>
      <p>{{ competencias }}</p>
      <p>Mi opinión hasta ahora del framework es:</p>
      <p>{{ opinion }}</p>
    </section>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  align-items: center;
  min-height: 100vh;
  column-gap: 1rem;
}

form {
  background-color: rgba(0, 0, 0, 0.89);
  color: lightgray;
  width: 40%;
  padding: 1rem;
  border-radius: .5rem;
}

label {
  margin-right: .5rem;
}

input, select {
  border-radius: .3rem;
  padding: .4rem;
}

ul {
  list-style-type: none;
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}

hr {
  margin-block: 1em;
}

.list {
  display: flex;
  column-gap: .5rem;
}

.opinion {
  display: flex;
}

textarea {
  width: 100%;
  height: 3rem;
  padding: .5rem;
  border-radius: .3rem;
}

section {
  border: 1px solid lightgray;
  width: 60%;
  padding: 1rem;
  border-radius: .5rem;
  text-align: center;
}

p {
  margin-block: .8rem;
}
</style>