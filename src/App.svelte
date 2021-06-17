<script>
  //   export let name;
</script>

<main>
  <img class="logo" src="./images/coliseumLogo.png" alt="logo" />
  <div class="wrapper">
    <img src="./images/title.png" alt="title" />
    <!-- <h1 class="title">Coliseum</h1> -->
    <form class="wrapper-login" action="">
      <input
        class="entry-data"
        placeholder="Username"
        type="text"
        name="name"
        required
      />
      <input
        class="entry-data"
        placeholder="Password"
        type="password"
        name="password"
        required
      />
      <input
        type="submit"
        class="button-login"
        data-submit="...Sending"
        value="Login"
      />
    </form>
    <div class="options">
      <a href="/">Register</a>
      <a href="/">I forgot my password</a>
      <a href="/">Description</a>
    </div>
  </div>
</main>

<style type="text/scss">
  @import "./styles/styles.scss";

  main {
    display: flex;
    justify-content: center;
    height: 100vh;
    background-color: #3a4151;
    .logo {
      position: absolute;
      top: 42px;
      left: clamp(50px, 3.95vw, 80px);
      width: clamp(60px, 4.16vw, 90px);
    }
    .wrapper {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-top: 244px;

      img {
        width: clamp(316px, 27.65vw, 600px);
      }

      &-login {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 80px;

        .entry-data {
          color: #c8c4c4;
          font-family: "Raleway", sans-serif;
          font-size: 15px;
          font-weight: 300;
          width: 343px;
          height: 35px;
          border-radius: 17px;
          border-style: none;
          margin-bottom: 15px;
          padding: 0 18px;
          background: #303643;
          box-shadow: inset 0px 4px 6px -2px rgba(0, 0, 0, 0.25);
          transition: all 0.3s ease-in-out;

          &:focus {
            box-shadow: inset 0px 0px 8px #15bdf8;
            outline: none;
            transition: all 0.3s ease-in-out;
          }

          &::placeholder {
            color: #c8c4c4;
            font-weight: 300;
          }
        }

        .button-login {
          width: 114px;
          height: 35px;
          border-radius: 17px;
          color: white;
          font-size: 15px;
          background: linear-gradient(
            183.88deg,
            #0dc8fc 3.18%,
            rgba(80, 112, 231, 0.9) 120.29%
          );
          box-shadow: 0px 0px 14px rgba(13, 200, 252, 0.6);
          border-style: none;
          cursor: pointer;
        }
      }

      .options {
        display: flex;
        justify-content: space-between;
        margin-top: 40px;
        width: clamp(330px, 21.45vw, 500px); // 412px

        a {
          font-size: 15px;
          font-weight: 300;
          color: white;
          text-decoration: none;

          &::after {
            content: "";
            display: block;
            height: 1px;
            width: 31px;
            margin: 5px auto 0;
            background: linear-gradient(
              90deg,
              rgba(23, 186, 248, 0.3) 3.33%,
              #3593ef 57.15%,
              rgba(80, 112, 231, 0.4) 106.67%
            );
          }
        }
      }
    }
  }
</style>
