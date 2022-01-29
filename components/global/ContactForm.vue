<template>
  <div class="form-wrapper grid">
    <div class="contact-content">
      <h1>Contact Me</h1>
      <p>Hey thanks for reaching out! Fill in this form, and I'll get back to you ASAP.</p>
    </div>
    <form name="contact" method="POST" data-netlify="true">
      <div class="input-wrapper">
        <div>
          <label>Name: <input type="text" name="name" /></label>   
        </div>
        <div>
          <label>Email: <input type="email" name="email" /></label>
        </div>
        <div>
          <label>Message: <textarea name="message"></textarea></label>
        </div>
        <div>
          <button type="submit">Send</button>
        </div>
      </div>
    </form>
  </div>
</template>

<style scoped lang="scss">
  form {
    width: 100%;
  }

  .input-wrapper {
    display: grid;
    gap: 16px;
  }

  label {
    font-size: 12px;
  }

  input {
    background: var(---background);
    border: 1px solid var(---text);
    color: var(---text);
    font-size: 16px;
    padding: 5px;
    width: 100%;
  }

  textarea {
    background: var(---background);
    border: 1px solid var(---text);
    display: block;
    color: var(---text);
    font-size: 16px;
    height: 150px;
    padding: 5px;
    resize: none;
    width: 100%;
  }

  button {
    appearance: none;
    background-color: var(---background);
    border: 2px solid var(---accent);
    color: var(---accent);
    cursor: pointer;
    display: block;
    padding: 5px;
    width: 100%;
  }
</style>