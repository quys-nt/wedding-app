<script>
  import svelteLogo from "../assets/images/main-visual-01.png";
</script>

<section class="mv">
  <img src={svelteLogo} class="mv-img" alt="main visual" />
  <div class="mv-bg"></div>
  <div class="mv-heading__wrapper">
    <h1 class="mv-heading__text">kỷ niệm ngày cưới</h1>
    <div class="mv-heading__contents">
      <p>Dĩ An <br /> Bình Dương</p>
      <p>Trung Tâm Hội Nghị <br /> Tiệc Cưới Thanh Tùng</p>
      <p>13-10-2024</p>
    </div>
  </div>
</section>

<style>
  .mv {
    position: relative;
    display: flex;
  }
  .mv-bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: linear-gradient(#0000001a, #00000096);
    color: #fff;
  }
  .mv-img {
    max-width: 100%;
  }
  @media screen and (max-width: 768px) {
    .mv-img {
      height: 640px;
      object-fit: cover;
      object-position: 33%;
    }
  }
  .mv-heading__wrapper {
    position: absolute;
    bottom: 2rem;
    left: 50%;
    width: 100%;
    height: 100%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: center;
    gap: 2rem;
    padding-inline: 12px;
  }
  .mv-heading__text {
    font-family: "Roboto Slab", serif;
    font-weight: 700;
    font-size: clamp(30px, 8vw, 100px);
    text-transform: uppercase;
  }
  .mv-heading__contents {
    font-family: "Dancing Script", cursive;
    display: flex;
    text-align: center;
    align-items: center;
  }
  .mv-heading__contents p {
    font-size: clamp(16px, 2vw, 22px);
    font-weight: 400;
  }
  .mv-heading__contents p:nth-child(2) {
    font-size: clamp(20px, 2vw, 30px);
    border: 1px solid #fff;
    border-top: 0;
    border-bottom: 0;
    padding-inline: 20px;
    margin-inline: 20px;
  }
  @media screen and (max-width: 768px) {
    .mv-heading__contents p:nth-child(2) {
      padding-inline: 10px;
      margin-inline: 10px;
    }
  }
</style>
