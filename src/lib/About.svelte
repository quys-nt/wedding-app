<script>
  import thiepcuoi01 from "../assets/images/wedding-qy-pa-thiep-cuoi-01.jpg";
  import thiepcuoi02 from "../assets/images/wedding-qy-pa-thiep-cuoi-02.jpg";
</script>

<section class="about">
  <div class="about__bg about__bg-01"></div>
  <div class="about__bg about__bg-02"></div>
  <div class="about__bg about__bg-03"></div>
  <div class="about__wrapper">
    <div class="save-day__wrapper">
      <div class="save-day__inner">
        <h2 class="save-day__heading">Save <span>The</span> Day</h2>
        <p class="save-day__heading-01">
          13.10<br />
          2024
        </p>
        <p class="save-day__heading-02">Phương Anh ♥ Thành Quý</p>
      </div>
    </div>
    <div class="about__wrapper--item">
      <img src={thiepcuoi01} alt="Thông tin ngày cưới 01" />
    </div>
    <div class="about__wrapper--item">
      <img src={thiepcuoi02} alt="Thông tin ngày cưới 02" />
    </div>
  </div>
</section>

<style>
  .about {
    position: relative;
    overflow: hidden;
    padding: 100px 12px;
  }
  @media screen and (max-width: 1024px) {
    .about {
      padding-top: 20px;
      padding-bottom: 0px;
    }
  }
  .about__bg {
    width: 400px;
    height: 400px;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    border-radius: 50%;
    filter: blur(150px);
  }
  @media screen and (max-width: 767px) {
    .about__bg {
      width: 200px;
      height: 200px;
    }
  }
  .about__bg-01 {
    right: 20%;
    background-color: #ff0d6a;
  }
  .about__bg-02 {
    left: 20%;
    background-color: #00ffe0;
  }
  .about__bg-03 {
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: #0500ff;
  }
  .about__wrapper {
    position: relative;
    display: grid;
    grid-template-columns: repeat(3, 860px);
    grid-template-rows: 600px;
    gap: 10px;
    overflow: auto;
  }
  .about__wrapper::-webkit-scrollbar {
    width: 0px;
  }
  .about__wrapper::-webkit-scrollbar-track {
    background: transparent;
  }
  .about__wrapper::-webkit-scrollbar-thumb {
    background: transparent;
  }
  ::-webkit-scrollbar-thumb:hover {
    background: transparent;
  }
  @media screen and (max-width: 1024px) {
    .about__wrapper {
      grid-template-columns: repeat(3, 540px);
      grid-template-rows: 400px;
    }
  }
  .about__wrapper--item {
    position: relative;
  }
  .about__wrapper img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
  }
  .save-day__wrapper {
    color: #000;
    height: 100%;
  }
  .save-day__inner {
    position: relative;
    height: 100%;
    padding: 40px;
    border: 1px solid #ccc;
    border-radius: 2px;
    text-align: center;
    background: #fff url("../assets/images/img-save-day-bg-02.png") no-repeat
      center;
    background-size: contain;
  }
  .save-day__heading {
    font:
      300 16px "Roboto Slab",
      serif;
    text-transform: uppercase;
  }
  .save-day__heading span {
    font:
      400 28px "Dancing Script",
      cursive;
    text-transform: capitalize;
  }
  .save-day__heading-01 {
    position: absolute;
    top: 50%;
    left: 50%;
    font:
      600 9rem "Dancing Script",
      cursive;
    transform: translate(-50%, -50%);
    color: #fbfafa;
    line-height: 1.2;
  }
  @media screen and (max-width: 1024px) {
    .save-day__heading-01 {
      font-size: 6rem;
    }
  }
  .save-day__heading-02 {
    position: absolute;
    top: 50%;
    left: 50%;
    font:
      400 5.4rem "Great Vibes",
      system-ui;
    transform: translate(-50%, -50%) rotate(-10deg);
    color: #b44a4d;
    white-space: nowrap;
  }
  @media screen and (max-width: 1024px) {
    .save-day__heading-02 {
      font-size: 3.5rem;
    }
  }
</style>
