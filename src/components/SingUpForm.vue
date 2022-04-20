<template lang="pug">
main
  h1 {{ title }}
  .form-container
    form
      div Enjoy the most wonderful time of the year one day at time
      input(type='text')
      label(for='email') Your email
      input(type='password')
      label(for='password') Your password
      button(type='submit') START RECEIVING YOUR GIFTS

    img(src='../assets/img/santagift.svg')
</template>

<script lang="ts">

export default {
  name: 'sing-up-form',
  data() {
    return {
      title: 'Advent Calendar'
    }
  }
}
</script>

<style scoped lang="scss">
  @import '../assets/styles/_variables.scss';

  main {
    background-color: $green-dark;
    width: 100%;
    height: 100%;

    h1 {
      font-family:  'Emilys Candy';
      font-style: normal;
      font-weight: 400;
      color: white;
      margin: 0;
      padding-top: 1.5rem;
      padding-bottom: 1.5rem;
      text-align: center;
    }

    .form-container {
      height: 100%;
      position: relative;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;

      img {
        position: absolute;
        top: 0;
      }

      form {
        padding-top: 4rem;
        width: 100%;
        background-color: $green-light;
        height: 100%;
        border-radius: $border-radius;
        position: absolute;
        top: 20%;
        z-index: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        font-family: 'Open Sans';
        font-style: normal;
        font-weight: 600;
        
        div {
          color: $black;
          width: 80%;
          text-align: center;
          padding-bottom: 1rem;
          padding-top: 1rem;
        }

        input {
          background: transparent;
          border: none;
          border-bottom: 2px solid $green-medium;
          width: 80%;
          margin-top: 2rem;
          font-size: 1.5rem;
          color: black;
        }

        input:focus {
          outline: none;
          border-bottom: 3px solid $green-medium;
          font-size: 1.7rem;
        }

        label {
          color: $green-medium;
          align-self: flex-start;
          width: 80%;
          padding-left: 10%;
          margin-bottom: 2rem;
        }

        button {
          margin-top: 2rem;
          margin-bottom: 1rem;
          border-radius: $border-radius;
          font-weight: 700;
          color: white;
          border: 2px solid white;
          padding: 1rem;
          background-color: $red-medium;
        }

        button:hover {
          background-color: $red-dark;
        }

        button:disabled {
          background-color: $gray;
        }
      }
    }


  }

</style>


