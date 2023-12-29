<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button :class="buttonClasses">A Stylex button!</button>
    <h3>Forked projeect from :</h3>
    <ul>
      <li>
        <a
          href="https://github.com/reacttips-dev/stylex"
          target="_blank"
          rel="noopener"
          >reacttips-dev/stylex</a
        >
      </li>
    </ul>

    <p>
      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >.
    </p>

    <hr />
    <h3 :class="heading">Sub Heading</h3>
    <button :class="buttonSubmit">Submit Button</button>
  </div>
</template>

<script>
import stylex from "@ladifire-opensource/stylex";

const styles = stylex.create({
  button: {
    borderRadius: 18,
    padding: 16,
    backgroundColor: "#1DA1F2",
    color: "#fff",
    borderColor: "#e3e312",
  },
  heading: {
    color: "blue",
    backgroundColor: "black",
    margin: "100px",
  },
});

const button_styles = stylex.create({
  base: {
    marginTop: "30px",
    border: "none",
    background: "none",
    padding: "20px 10px",
    bordedrRadius: ".25em",
    cursor: "pointer",
  },
  variant: {
    color: "white",
    backgroundColor: "#00AAFF",
  },
  danger: {
    color: "white",
    backgroundColor: "#FF0000",
  },
});

export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  computed: {
    buttonClasses() {
      return stylex(styles.button);
    },
    heading() {
      return stylex(styles.heading);
    },
    buttonSubmit() {
      return stylex(button_styles.base, button_styles.danger);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
