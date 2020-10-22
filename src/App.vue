<template>
  <div id="app">
    <h1>Buttons</h1>

    <div class="showcase">
      <div class="row">
        <div class="button-container">
          <ButtonLabel content='Button content="Click here"' />
          <Button content="Click here" />
        </div>
      </div>

      <div class="row">
        <div class="button-container">
          <ButtonLabel content='Button variant="outline"' />
          <Button variant="outline" />
        </div>
      </div>

      <div class="row">
        <div class="button-container">
          <ButtonLabel content='Button variant="text"' />
          <Button variant="text" />
        </div>
      </div>

      <div class="row">
        <div class="button-container">
          <ButtonLabel content="Button disableShadow" />
          <Button disableShadow />
        </div>
      </div>

      <div class="row">
        <div class="button-container">
          <ButtonLabel content="Button disabled" />
          <Button disabled />
        </div>

        <div class="button-container">
          <ButtonLabel content='Button variant="text" disabled' />
          <Button variant="text" disabled />
        </div>
      </div>

      <div class="row">
        <div class="button-container">
          <ButtonLabel content='Button startIcon="local_grocery_store"' />
          <Button startIcon="local_grocery_store" />
        </div>

        <div class="button-container">
          <ButtonLabel content='Button endIcon="local_grocery_store"' />
          <Button endIcon="local_grocery_store" />
        </div>
      </div>

      <div class="row">
        <div class="button-container">
          <ButtonLabel content='Button size="sm"' />
          <Button size="sm" />
        </div>

        <div class="button-container">
          <ButtonLabel content='Button size="md"' />
          <Button size="md" />
        </div>

        <div class="button-container">
          <ButtonLabel content='Button size="lg"' />
          <Button size="lg" />
        </div>
      </div>

      <div class="row">
        <div class="button-container">
          <ButtonLabel content='Button color="default' />
          <Button color="default" />
        </div>

        <div class="button-container">
          <ButtonLabel content='Button color="primary' />
          <Button color="primary" />
        </div>

        <div class="button-container">
          <ButtonLabel content='Button color="secondary' />
          <Button color="secondary" />
        </div>

        <div class="button-container">
          <ButtonLabel content='Button color="danger' />
          <Button color="danger" />
        </div>
      </div>
    </div>

    <footer>
      Icons:
      <a href="https://material.io/resources/icons/?style=baseline">
        material.io/resources/icons/?style=baseline
      </a>

      <p>Matheus Carvalho @DevChallenges.io</p>
    </footer>
  </div>
</template>

<script>
import Button from "./components/Button";
import ButtonLabel from "./components/Button-Label";

export default {
  name: "App",
  components: {
    Button,
    ButtonLabel,
  },
};
</script>

<style>
#app {
  padding: 30px 80px 0;
}

h1 {
  font-family: "Poppins";
  font-weight: 500;
  font-size: 24px;
  line-height: 36px;

  color: #4f4f4f;

  margin-bottom: 20px;
}

.row {
  display: flex;
  align-items: center;

  margin-bottom: 40px;
}

.button-container {
  margin-right: 45px;
}

footer,
footer p,
footer a {
  font-family: "Ubuntu Mono";
  font-size: 15px;
  line-height: 12px;
  text-decoration: none;

  color: #828282;

  margin-top: 10px;
}

footer p {
  text-align: center;
}
</style>
