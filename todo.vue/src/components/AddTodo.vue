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