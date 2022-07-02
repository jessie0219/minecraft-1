<template>
  <div class="container-fluid news p-5">
    <div class="row d-flex justify-content-center">
      <h3 class="display-5 fw-bold mb-5 text-center">最新消息</h3>
      <div class="col col-md-10 col-lg-10 accordion" id="accordionExample">
        <div class="accordion-item">
          <h2 class="accordion-header" id="headingOne">
            <button
              class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#collapseOne"
              aria-expanded="true"
              aria-controls="collapseOne"
            >
              <div class="date px-2 py-1 text-light">2022/05/17</div>
              【邀請賽-FINAL延期公告】
            </button>
          </h2>
          <div
            id="collapseOne"
            class="accordion-collapse collapse"
            aria-labelledby="headingOne"
            data-bs-parent="#accordionExample"
          >
            <div class="accordion-body f-2">
              依照中央疫情指揮中心推估疫情發展，本波疫情確診高峰將落在五月底六月初，加上國小學童於本月陸續開始施打疫苗，預計七月後疫情緩解時，再舉辦實體活動家長較為放心，本會與各合辦學校會議後決定，今年邀請賽最後一次延期，目前確定時間如無法執行，則轉成線上競賽實體頒獎舉辦。 
              <ul>
                <li>北護場 08/27 舉辦</li>
                <li>文大場 9/4 舉辦</li>
                <li>明道場暑假後待定</li>
                <li>真理場暑假後待定</li>
              </ul>

    

    

    

    
            </div>
          </div>
        </div>
        <div class="accordion-item">
          <h2 class="accordion-header" id="headingTwo">
            <button
              class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#collapseTwo"
              aria-expanded="false"
              aria-controls="collapseTwo"
            >
              <div class="date px-2 py-1 text-light">2022/OO/OO</div>
              【Lorem ipsum dolor, sit amet consectetur adipisicing elit.】 
            </button>
          </h2>
          <div
            id="collapseTwo"
            class="accordion-collapse collapse"
            aria-labelledby="headingTwo"
            data-bs-parent="#accordionExample"
          >
            <div class="accordion-body">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. In, soluta mollitia quo tenetur, voluptate quaerat, minus delectus dolore assumenda vel quod est facilis sed similique tempora quisquam eum iure eveniet?
            </div>
          </div>
        </div>
        <div class="accordion-item">
          <h2 class="accordion-header" id="headingThree">
            <button
              class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#collapseThree"
              aria-expanded="false"
              aria-controls="collapseThree"
            >
              <div class="date px-2 py-1 text-light">2022/OO/OO</div>
              【Lorem ipsum dolor, sit amet consectetur adipisicing elit.】 
            </button>
          </h2>
          <div
            id="collapseThree"
            class="accordion-collapse collapse"
            aria-labelledby="headingThree"
            data-bs-parent="#accordionExample"
          >
            <div class="accordion-body">
              Lorem ipsum dolor, sit amet consectetur adipisicing elit. Cupiditate neque sapiente mollitia quos ut alias quae ex repudiandae reiciendis, officia ad voluptatibus odit rerum minima dolorum itaque possimus eaque saepe.
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LatestNews",
};
</script>

<style scoped>

button .date {
  background-color: rgba(39, 146, 39, 0.705);
  border-radius: 50px;
}
</style>
