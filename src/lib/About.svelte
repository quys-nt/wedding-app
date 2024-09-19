<script>
  import thiepcuoi01 from "../assets/images/wedding-qy-pa-thiep-cuoi-01.jpg";
  import thiepcuoi02 from "../assets/images/wedding-qy-pa-thiep-cuoi-02.jpg";
</script>

<section class="about">
  <div class="about__bg about__bg-01"></div>
  <div class="about__bg about__bg-02"></div>
  <div class="about__bg about__bg-03"></div>
  <div class="about__wrapper">
    <img src={thiepcuoi01} alt="Thông tin ngày cưới 01" />
    <img src={thiepcuoi02} alt="Thông tin ngày cưới 02" />
  </div>
</section>

<style>
  .about {
    position: relative;
    overflow: hidden;
    padding: 100px 12px;
  }
  @media screen and (max-width: 767px) {
    .about {
      padding-block: 20px;
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
    grid-template-columns: 1fr 1fr;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    max-width: 1440px;
    margin-inline: auto;
  }
  @media screen and (max-width: 1200px) {
    .about__wrapper {
      grid-template-columns: 1fr;
    }
  }
</style>
