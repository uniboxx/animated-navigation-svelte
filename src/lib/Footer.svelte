<footer>
  <div class="about">
    <p>By unibox - 2024</p>
    <div class="social">
      <i class="fa-brands fa-telegram" aria-hidden="true"></i>
      <p><a href="https://t.me/unibox" target="_blank">t.me/unibox</a></p>
    </div>
  </div>
</footer>

<style lang="scss">
  footer {
    background-color: secondary-color;
    color: #fff;
    display: flex;
    justify-content: end;
    align-items: center;
    padding: 20px 30px;
  }
  .about {
    p {
      padding: 0;
      margin: 0;
      font-size: 1.1rem;

      a {
        cursor: pointer;
        color: inherit;
        text-decoration: none;
        &:hover {
          color: #aaa;
        }
      }
    }
    .social {
      display: flex;
      margin: 10px;
      .fa-telegram {
        font-size: 25px;
        margin: 0 10px;
      }
    }
  }
</style>
