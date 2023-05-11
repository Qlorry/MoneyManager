<script setup lang="ts">
</script>

<template>
  <div class="container">
    <div class="row mt-3">

      <div class="col-md-4 col-sm-12">
        <div class="card">
          <div class="card-header">
            <h2 class="text-center ">Add purchase</h2>
          </div>

          <div class="card-body">
            <div class="text-center fs-5  mb-2">Bill</div>

            <ul class="list-group">
              <li class="list-group-item">
                <input class="form-control mb-1" type="text" placeholder="Purchase name" aria-label="Purchase name">

                <div class="d-flex flex-row align-items-center ps-2">
                  <div class="me-2"> Price: </div>
                  <input class="form-control flex-grow" type="text" placeholder="Price" aria-label="Purchase name">

                </div>
                <!-- <h5 class="mb-1">List group item heading</h5> -->
              </li>
              <li class="list-group-item">
                <input class="form-control mb-1" type="text" placeholder="Purchase name" aria-label="Purchase name">

                <div class="d-flex flex-row align-items-center ps-2">
                  <div class="me-2"> Price: </div>
                  <input class="form-control flex-grow" type="text" placeholder="Price" aria-label="Purchase name">

                </div>
                <!-- <h5 class="mb-1">List group item heading</h5> -->
              </li>
              <li class="list-group-item">
                <button type="button" class="btn btn-success w-100">Add another item</button>
              </li>
            </ul>

            <div class="text-center fs-5 my-2">Payers</div>


            <select class="form-select" multiple aria-label="multiple select example">
              <option value="1">Dima</option>
              <option value="2">Koka</option>
              <option value="3">Anton</option>
            </select>
            <div class="btn-group w-100 mt-2" role="group" aria-label="Basic example">
              <button type="button" class="btn btn-outline-primary">Select All</button>
              <button type="button" class="btn btn-outline-primary">Deselect All</button>
            </div>

            <button type="button" class="btn btn-success w-100 my-2">Submit</button>
          </div>
        </div>
      </div>

      <div class="col-md-8 col-sm-12">
        <div class="card">
          <div class="card-header">
            <h2 class="">My Dept</h2>
          </div>

          <div class="card-body">
            <div class="row">
              <div class="col-md-5 col-sm-12">
                <div class="overflow-auto" style="max-height: 400px;">
                  <div class="accordion" id="accordionExample">
                    <div class="accordion-item">
                      <h2 class="accordion-header">
                        <button class="accordion-button" type="button" data-bs-toggle="collapse"
                          data-bs-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
                          <div class="d-flex flex-column">
                            <div class="fs-5">To Dima</div>
                            <div class="d-flex gap-2 mt-1">

                              <div class="p-2 border border-secondary rounded">Raw: 100000</div>
                              <div class="p-2 border border-secondary rounded">Total: 1000</div>
                            </div>
                          </div>

                        </button>
                      </h2>
                      <div id="collapseOne" class="accordion-collapse collapse show" data-bs-parent="#accordionExample">
                        <div class="accordion-body">
                          <ul class="list-group">
                            <li class="list-group-item d-flex justify-content-between align-items-center">
                              A list item
                              <span class="badge bg-primary rounded-pill">14</span>
                            </li>
                            <li class="list-group-item d-flex justify-content-between align-items-center">
                              A second list item
                              <span class="badge bg-primary rounded-pill">2</span>
                            </li>
                            <li class="list-group-item d-flex justify-content-between align-items-center">
                              A third list item
                              <span class="badge bg-primary rounded-pill">1</span>
                            </li>
                          </ul>

                          <div class="d-flex flex-row align-items-center ps-2 pt-2">
                            <div class="me-2"> Pay: </div><input class="form-control flex-grow" type="text"
                              placeholder="Amount" aria-label="Purchase name">
                          </div>
                          <button type="button" class="btn btn-success w-100 my-2">Submit</button>
                        </div>
                      </div>
                    </div>
                    <div class="accordion-item">
                      <h2 class="accordion-header">
                        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                          data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                          <div class="d-flex flex-column">
                            <div class="fs-5">To Anton</div>
                            <div class="d-flex gap-2 mt-1">

                              <div class="p-2 border border-secondary rounded">Raw: 100000</div>
                              <div class="p-2 border border-secondary rounded">Total: 1000</div>
                            </div>
                          </div>
                        </button>
                      </h2>
                      <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                        <div class="accordion-body">
                          <strong>This is the second item's accordion body.</strong> It is hidden by default, until the
                          collapse plugin adds the appropriate classes that we use to style each element. These classes
                          control the overall appearance, as well as the showing and hiding via CSS transitions. You can
                          modify any of this with custom CSS or overriding our default variables. It's also worth noting
                          that just about any HTML can go within the <code>.accordion-body</code>, though the transition
                          does limit overflow.
                        </div>
                      </div>
                    </div>
                    <div class="accordion-item">
                      <h2 class="accordion-header">
                        <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                          data-bs-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                          <div class="d-flex flex-column">
                            <div class="fs-5">To Koka</div>
                            <div class="d-flex gap-2 mt-1">

                              <div class="p-2 border border-secondary rounded">Raw: 100000</div>
                              <div class="p-2 border border-secondary rounded">Total: 1000</div>
                            </div>
                          </div>
                        </button>
                      </h2>
                      <div id="collapseThree" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                        <div class="accordion-body">
                          <strong>This is the third item's accordion body.</strong> It is hidden by default, until the
                          collapse plugin adds the appropriate classes that we use to style each element. These classes
                          control the overall appearance, as well as the showing and hiding via CSS transitions. You can
                          modify any of this with custom CSS or overriding our default variables. It's also worth noting
                          that just about any HTML can go within the <code>.accordion-body</code>, though the transition
                          does limit overflow.
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-md-7 col-sm-12">

              </div>
            </div>

          </div>
        </div>
        <div class="card mt-3">
          <div class="card-header">
            <h2 class="">My Credits</h2>
          </div>

          <div class="card-body">
            <div class="row">
              <div class="col-5">
                <div class="overflow-auto" style="max-height: 400px;">
                  <ul class="list-group">
                    <li class="list-group-item">
                      <div class="d-flex flex-column">
                        <div class="fs-5">To Dima</div>
                        <div class="d-flex gap-2 mt-1">

                          <div class="p-2 flex-grow-1 text-center border border-secondary rounded">Raw: 100000</div>
                          <div class="p-2 flex-grow-1 text-center border border-secondary rounded">Total: 1000</div>
                        </div>
                      </div>
                    </li>
                    <li class="list-group-item">A second item</li>
                    <li class="list-group-item">A third item</li>
                    <li class="list-group-item">A fourth item</li>
                    <li class="list-group-item">And a fifth one</li>
                  </ul>
                </div>
              </div>
              <div class="col-7">

              </div>
            </div>

          </div>
        </div>
      </div>
    </div>

  </div>
</template>
