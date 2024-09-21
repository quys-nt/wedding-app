<section class="save-day">
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
</section>

<style>
  .save-day {
    color: #000;
  }
  .save-day__wrapper {
    max-width: 890px;
    margin: 40px auto;
    padding-inline: 12px;
  }
  .save-day__inner {
    position: relative;
    min-height: 500px;
    padding: 40px;
    border: 1px solid #ccc;
    border-radius: 2px;
    text-align: center;
    background: url("../assets/images/img-save-day-bg-02.png") no-repeat center;
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
      600 6rem "Dancing Script",
      cursive;
    transform: translate(-50%, -50%);
    color: #fbfafa;
    line-height: 1.2;
  }

  .save-day__heading-02 {
    position: absolute;
    top: 50%;
    left: 50%;
    font:
      400 5rem "Great Vibes",
      system-ui;
    transform: translate(-50%, -50%) rotate(-10deg);
    color: #b44a4d;
    white-space: nowrap;
  }
</style>
