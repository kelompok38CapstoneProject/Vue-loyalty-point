<template>
  <div>
    <!-- <div class="col-12 text-right">
      <a class="btn btn-primary mb-3 mr-2" role="button" data-slide="prev">
        <i class="fa fa-chevron-left"></i>
      </a>
      <a class="btn btn-primary mb-3" role="button" data-slide="next">
        <i class="fa fa-chevron-right"></i>
      </a>
    </div> -->
    <b-carousel
      id="multipleItems"
      v-model="slide"
      :interval="400000"
      controls
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide>
        <template v-slot:img>
          <b-card-group>
            <div class="col-lg-4 col-sm-12">
              <b-card class="card-list-g shadow-sm">
                <h5 class="text-md">Telkomsel</h5>
                <ul class="list-group list-group-flush d-flex">
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #62c91e">
                      Stock Ready
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #d4bb00">
                      Low Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #f23030">
                      Out Of Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                </ul>
              </b-card>
            </div>
            <div class="col-lg-4 col-sm-12">
              <b-card class="card-list-g shadow-sm">
                <h5 class="text-md">Telkomsel</h5>
                <ul class="list-group list-group-flush d-flex">
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #62c91e">
                      Stock Ready
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #d4bb00">
                      Low Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #f23030">
                      Out Of Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                </ul>
              </b-card>
            </div>
            <div class="col-lg-4 col-sm-12">
              <b-card class="card-list-g shadow-sm">
                <h5 class="text-md">Telkomsel</h5>
                <ul class="list-group list-group-flush d-flex">
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #62c91e">
                      Stock Ready
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #d4bb00">
                      Low Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #f23030">
                      Out Of Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                </ul>
              </b-card>
            </div>
          </b-card-group>
        </template>
      </b-carousel-slide>

      <b-carousel-slide>
        <template v-slot:img>
          <b-card-group>
            <div class="col-lg-4 col-sm-12">
              <b-card class="card-list-g shadow-sm">
                <h5 class="text-md">Telkomsel</h5>
                <ul class="list-group list-group-flush d-flex">
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #62c91e">
                      Stock Ready
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #d4bb00">
                      Low Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #f23030">
                      Out Of Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                </ul>
              </b-card>
            </div>
            <div class="col-lg-4 col-sm-12">
              <b-card class="card-list-g shadow-sm">
                <h5 class="text-md">Telkomsel</h5>
                <ul class="list-group list-group-flush d-flex">
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #62c91e">
                      Stock Ready
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #d4bb00">
                      Low Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #f23030">
                      Out Of Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                </ul>
              </b-card>
            </div>
            <div class="col-lg-4 col-sm-12">
              <b-card class="card-list-g shadow-sm">
                <h5 class="text-md">Telkomsel</h5>
                <ul class="list-group list-group-flush d-flex">
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #62c91e">
                      Stock Ready
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #d4bb00">
                      Low Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                  <li
                    class="
                      list-group-item
                      d-flex
                      align-items-center
                      justify-content-between
                    "
                  >
                    <div class="text-base" style="color: #f23030">
                      Out Of Stock
                    </div>
                    <div class="text-md">01</div>
                  </li>
                </ul>
              </b-card>
            </div>
          </b-card-group>
        </template>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  data: () => ({
    slide: 0,
    sliding: null,
  }),
  methods: {
    onSlideStart(slide) {
      this.sliding = true
    },
    onSlideEnd(slide) {
      this.sliding = false
    },
  },
}
</script>

<style>
#multipleItems .carousel-inner {
  width: 80%;
  margin-left: auto;
  margin-right: auto;
}
#multipleItems .carousel-control-prev,
#multipleItems .carousel-control-next {
  width: 10%;
}
#multipleItems .carousel-control-prev-icon {
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' fill='%234e73df' width='24' height='24' viewBox='0 0 8 8'%3e%3cpath d='M5.25 0l-4 4 4 4 1.5-1.5L4.25 4l2.5-2.5L5.25 0z'/%3e%3c/svg%3e");
}
#multipleItems .carousel-control-next-icon {
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' fill='%234e73df' width='24' height='24' viewBox='0 0 8 8'%3e%3cpath d='M2.75 0l-1.5 1.5L3.75 4l-2.5 2.5L2.75 8l4-4-4-4z'/%3e%3c/svg%3e");
}
.carousel-control-prev {
  left: 900px;
  margin-top: -330px;
  /* margin-left: 180px; */
    
}
.carousel-control-next {
  right: 0;
  margin-top: -330px;
  /* margin-right: 90px; */
}
.carousel {
    position: auto;
    /* margin-left: -150px;
    margin-right: -150px; */
}
</style>