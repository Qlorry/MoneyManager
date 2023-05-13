<script setup lang="ts">

</script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-md-4 col-sm-12 mt-3">
        <div class="card">
          <div class="card-header">
            <h2 class="text-center ">New trip</h2>
          </div>

          <div class="card-body">
            <input class="form-control mb-1" type="text" placeholder="Trip name" aria-label="Purchase name">

            <ul class="list-group">
              <li class="list-group-item">Koka</li>
              <li class="list-group-item">Lena</li>
              <li class="list-group-item">Anton</li>
              <li class="list-group-item">
                <select class="form-select" aria-label="Select Users Here">
                  <option selected>Select Users Here</option>
                  <option value="1">One</option>
                  <option value="2">Two</option>
                  <option value="3">Three</option>
                </select>
              </li>
            </ul>

            <button type="button" class="btn btn-success w-100 my-2">Submit</button>
          </div>
        </div>
      </div>

      <div class="col-md-4 col-sm-12 mt-3">
        <div class="card">
          <div class="card-header">
            <h2 class="text-center ">Active Trips</h2>
          </div>

          <div class="card-body">

            <ul class="list-group">
              <li class="list-group-item">
                <RouterLink to="/" class="nav-link active text-light">aaa</RouterLink>
              </li>
              <li class="list-group-item">
                <RouterLink to="/" class="nav-link active text-light">aaa</RouterLink>
              </li>
              <li class="list-group-item">
                <RouterLink to="/" class="nav-link active text-light">aaa</RouterLink>
              </li>
            </ul>
          </div>
        </div>
      </div>

      <div class="col-md-4 col-sm-12 mt-3">
        <div class="card">
          <div class="card-header">
            <h2 class="text-center ">My Trips</h2>
          </div>

          <div class="card-body">

            <div class="accordion" id="accordionExample">

              <div class="accordion-item">
                <h2 class="accordion-header">
                  <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
                    data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                    Accordion Item #2
                  </button>
                </h2>

                <div id="collapseTwo" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                  <div class="accordion-body">
                    Users
                    <ul class="list-group overflow-y-auto" style="max-height: 200px;">
                      <li class="list-group-item">
                        <div class="d-flex flex-row align-items-center justify-content-between">
                          Name
                          <button type="button" class="btn btn-danger">Delete</button>
                        </div>
                      </li>
                    </ul>
                    Add new user
                    <select class="form-select mt-2" aria-label="Select Users Here">
                      <option selected>Select Users Here</option>
                      <option value="1">One</option>
                      <option value="2">Two</option>
                      <option value="3">Three</option>
                    </select>

                    <button type="button" class="btn w-100 mt-4 btn-danger">Delete Trip</button>

                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>
