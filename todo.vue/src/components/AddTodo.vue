<template>
  <section className="input-section">
    <section className="input-name">
      <input
        type="text"
        className="todo-input"
        placeholder="Enter your todo item"
      />
      <button className="add-btn">
        +
      </button>
    </section>
    <p className="alert-error" style={alertState}>
      Please input something first.
    </p>
  </section>
</template>

<style>
body,
html,
ul,
ol,
h1,
p {
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 1rem;
  color: #343a40;
  background-color: #fff;
  line-height: 1.5;
}

* {
  box-sizing: border-box;
}

ul,
ol {
  list-style-type: none;
}

.input-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.input-section .input-name {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.input-section .input-name input {
  height: 3rem;
  vertical-align: bottom;
  border: 1px solid #a9a9a9;
  border-radius: 3px;
  padding-left: 1rem;
  font-size: 1.25rem;
  flex: 1;
}
.input-section .input-name input:focus {
  outline: 0;
  border: 1px solid #7dced5;
}
.input-section .input-name button {
  width: 3rem;
  height: 3rem;
  margin-left: 0.5rem;
  border: none;
  border-radius: 0.2rem;
  background-color: #7dced5;
  text-align: center;
  color: white;
  font-size: 2rem;
}
.input-section .input-name button:active {
  background-color: #31c5d3;
}
.input-section .alert-error {
  background-color: #fff2f0;
  border: 1px solid #ffccc7;
  padding: 8px 15px;
  border-radius: 2px;
}
</style>