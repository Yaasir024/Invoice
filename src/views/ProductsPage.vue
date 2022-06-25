// https://codepen.io/TurkAysenur/pen/NWRqoyL //
https://codepen.io/abyeidengdit/pen/gOvjjWx?editors=1100 //
https://codepen.io/hanibal/details/PoQbyZO

<template>
  <div class="products-section">
    <div class="section-header">
      <p>Products</p>
      <div class="search-wrapper">
        <input type="text" placeholder="search" class="search" />
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="20"
          height="20"
          fill="none"
          stroke="currentColor"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          viewBox="0 0 24 24"
        >
          <defs></defs>
          <circle cx="11" cy="11" r="8"></circle>
          <path d="M21 21l-4.35-4.35"></path>
        </svg>
      </div>
      <button class="settings-btn" @click="openModal">
        <svg
          class="btn-icon"
          xmlns="http://www.w3.org/2000/svg"
          width="16"
          height="16"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="3"
          stroke-linecap="round"
          stroke-linejoin="round"
        >
          <line x1="12" y1="5" x2="12" y2="19" data-v-279ff09a=""></line>
          <line x1="5" y1="12" x2="19" y2="12" data-v-279ff09a=""></line>
        </svg>
      </button>
    </div>
    <!-- Activity Links -->
    <div class="activity-links">
      <div class="select-filter">
        <select class="select">
          <option value="0">Filter by Stock Status</option>
          <option value="1">In Stock</option>
          <option value="2">Out of Stock</option>
        </select>
      </div>
      <button class="filter-btn">Filter</button>
    </div>
    <!-- products container -->
    <div class="products-container">
      <table class="table">
        <tr class="table-header">
          <th>Id</th>
          <th>Name</th>
          <th>Price</th>
          <th>Quantity in Stock</th>
          <th>Variations</th>
          <th>Date Updated</th>
          <th></th>
        </tr>
        <tr>
          <td>#0001</td>
          <td>ZEALOT Headphone</td>
          <td>$400</td>
          <td>12 in Stock</td>
          <td>04</td>
          <td>04/12/2021</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#0002</td>
          <td>Dr DRE Headphone</td>
          <td>$800</td>
          <td>1 in Stock</td>
          <td>02</td>
          <td>08/12/2021</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#0003</td>
          <td>iPhone 13 pro max</td>
          <td>$900</td>
          <td>14 in Stock</td>
          <td>04</td>
          <td>04/11/2021</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#0004</td>
          <td>M2 pro</td>
          <td>$1600</td>
          <td>22 in Stock</td>
          <td>03</td>
          <td>07/07/2022</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#0005</td>
          <td>Apple Ear buds</td>
          <td>$400</td>
          <td>12 in Stock</td>
          <td>04</td>
          <td>04/12/2021</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#0008</td>
          <td>Samsung Headphone</td>
          <td>$400</td>
          <td>12 in Stock</td>
          <td>04</td>
          <td>04/12/2021</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#0009</td>
          <td>Redimi 2</td>
          <td>$1600</td>
          <td>20 in Stock</td>
          <td>03</td>
          <td>08/07/2022</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#0010</td>
          <td>Samsung A03s</td>
          <td>$200</td>
          <td>5 in Stock</td>
          <td>02</td>
          <td>07/07/2021</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#00011</td>
          <td>HP ProBook</td>
          <td>$1600</td>
          <td>0 in Stock</td>
          <td>03</td>
          <td>08/07/2022</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#00012</td>
          <td>KeyChron Keyboard</td>
          <td>$1200</td>
          <td>02 in Stock</td>
          <td>01</td>
          <td>07/04/2022</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
        <tr>
          <td>#00013</td>
          <td>Tech Mouse</td>
          <td>$400</td>
          <td>05 in Stock</td>
          <td>03</td>
          <td>09/07/2022</td>
          <td>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="20"
              height="20"
              class="edit-icon"
            >
              <path
                d="M421.7 220.3L188.5 453.4L154.6 419.5L158.1 416H112C103.2 416 96 408.8 96 400V353.9L92.51 357.4C87.78 362.2 84.31 368 82.42 374.4L59.44 452.6L137.6 429.6C143.1 427.7 149.8 424.2 154.6 419.5L188.5 453.4C178.1 463.8 165.2 471.5 151.1 475.6L30.77 511C22.35 513.5 13.24 511.2 7.03 504.1C.8198 498.8-1.502 489.7 .976 481.2L36.37 360.9C40.53 346.8 48.16 333.9 58.57 323.5L291.7 90.34L421.7 220.3zM492.7 58.75C517.7 83.74 517.7 124.3 492.7 149.3L444.3 197.7L314.3 67.72L362.7 19.32C387.7-5.678 428.3-5.678 453.3 19.32L492.7 58.75z"
              />
            </svg>
          </td>
        </tr>
      </table>
    </div>
  </div>
  <CreateProductModal :openAddModal="openAddModal" @closeAddModal="openModal"/>
</template>

<script setup>
/*
  imports
  */
import CreateProductModal from "@/components/modals/CreateProductModal.vue";
import { ref, reactive } from "vue";
/*
Add product Modal
*/
const openAddModal = ref(false)
const openModal = () => {
  openAddModal.value = !openAddModal.value
}
</script>

<style scoped>
.products-section {
  background: var(--dark-color2);
  padding: 40px 30px;
  width: 100%;
  overflow: hidden;
  border-radius: 32px;
}
/* Section Header */
.section-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.section-header p {
  font-size: 24px;
  font-weight: 700;
  opacity: 0.9;
}
.search-wrapper {
  background: #212752;
  border-radius: 18px;
  padding-right: 12px;
  height: 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  max-width: 480px;
  color: var(--text-color);
  overflow: hidden;
}
.search-wrapper .search {
  border: none;
  flex: 1;
  outline: none;
  height: 100%;
  padding: 0 20px;
  font-size: 16px;
  background-color: #212752;
  color: var(--text-color);
}
.settings-btn {
  color: #fff;
  cursor: pointer;
  background-color: #212752;
  padding: 0;
  border: 0;
  border-radius: 50%;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
}
/* Activity Links */
.activity-links {
  margin-top: 40px;
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
/* Filter */
select {
  height: 32px;
  color: var(--text-color);
  background: #212752;
}
.filter-btn {
  color: #fff;
  cursor: pointer;
  background-color: #212752;
  padding: 0;
  border: 0;
  padding: 10px 20px;
  margin-left: 20px;
  font-size: 15px;
}

/* Order content */
.products-container {
  margin-top: 20px;
  padding: 0 20px;
  display: block;
  max-height: 420px;
  overflow-y: auto;
}
.edit-icon {
  color: var(--text-color);
  fill: currentColor;
  cursor: pointer;
}
.products-container table {
  width: 100%;
  border-collapse: collapse;
}
.products-container .table-header {
  background-color: #212752;
  position: sticky;
  top: 0;
  z-index: 1;
}
.products-container th {
  text-align: left;
  padding: 5px;
}
.products-container td {
  padding: 15px 5px;
}
tr {
  min-height: 50px;
}
</style>
