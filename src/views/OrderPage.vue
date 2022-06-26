<template>
  <div class="orders-section">
    <div class="section-content">
      <div class="section-header">
        <p>Orders</p>
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
        <button class="add-btn" @click="toggleCreateModal">
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
            <line x1="12" y1="5" x2="12" y2="19"></line>
            <line x1="5" y1="12" x2="19" y2="12"></line>
          </svg>
        </button>
      </div>
    </div>
    <!-- Activity Link -->
    <div class="activity-links">
      <div
        class="activity-link all"
        @click="filter('all')"
        :class="filterValue == 'all' ? 'active' : ''"
      >
        All
      </div>
      <div
        class="activity-link completed"
        @click="filter('completed')"
        :class="filterValue == 'completed' ? 'active' : ''"
      >
        Completed
      </div>
      <div
        class="activity-link pending"
        @click="filter('pending')"
        :class="filterValue == 'pending' ? 'active' : ''"
      >
        Pending
      </div>
      <div
        class="activity-link cancelled"
        @click="filter('cancelled')"
        :class="filterValue == 'cancelled' ? 'active' : ''"
      >
        Cancelled
      </div>
    </div>
    <!-- Orders container -->
    <div class="orders-container">
      <table class="table">
        <tr class="table-header">
          <th>Id</th>
          <th>Order Id</th>
          <th>Invoice Id</th>
          <th>Name</th>
          <th>Date</th>
          <th>Status</th>
          <th></th>
        </tr>
        <tr v-for="(order, index) in orderList" :key="order.orderId">
          <td>{{ incrementIndex(index) }}</td>
          <td>{{ order.orderId }}</td>
          <td>{{ order.invoiceId }}</td>
          <td>
            {{ order.customerName }}
          </td>
          <td>{{ order.date }}</td>
          <td>
            <div
              class="status status-completed"
              v-if="order.status == 'completed'"
            >
              <svg
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <path d="M20 6L9 17l-5-5"></path>
              </svg>
              Completed
            </div>
            <div class="status status-pending" v-if="order.status == 'pending'">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="feather feather-loader"
              >
                <path
                  d="M12 2v4M12 18v4M4.93 4.93l2.83 2.83M16.24 16.24l2.83 2.83M2 12h4M18 12h4M4.93 19.07l2.83-2.83M16.24 7.76l2.83-2.83"
                ></path>
              </svg>
              Pending
            </div>
            <div
              class="status status-cancelled"
              v-if="order.status == 'cancelled'"
            >
              <svg
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <path d="M18 6L6 18M6 6l12 12"></path>
              </svg>
              Cancelled
            </div>
          </td>
          <td>
            <div class="option">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 128 512"
                width="20"
                height="20"
                class="option-icon"
              >
                <path
                  d="M64 360C94.93 360 120 385.1 120 416C120 446.9 94.93 472 64 472C33.07 472 8 446.9 8 416C8 385.1 33.07 360 64 360zM64 200C94.93 200 120 225.1 120 256C120 286.9 94.93 312 64 312C33.07 312 8 286.9 8 256C8 225.1 33.07 200 64 200zM64 152C33.07 152 8 126.9 8 96C8 65.07 33.07 40 64 40C94.93 40 120 65.07 120 96C120 126.9 94.93 152 64 152z"
                />
              </svg>
              <div class="option-menu">
                <div class="menu-item" @click="toggleEditModal(order.orderId)">
                  Edit
                </div>
                <div class="menu-item">Cancel</div>
                <div class="menu-item">Delete</div>
              </div>
            </div>
          </td>
        </tr>
      </table>
    </div>
  </div>
  <OrderModal
    :showModal="showModal"
    :createModal="createModal"
    :editModal="editModal"
    :editOrderId="editOrderId"
    @closeCreateModal="toggleCreateModal"
    @closeEditModal="toggleEditModal"
  />
</template>

<script setup>
/*
  imports
  */
import OrderModal from "@/components/modals/OrderModal.vue";
import { ref, reactive } from "vue";
/*
Toggle Show Modal
*/
const filterValue = ref("completed");
const filter = (value) => {
  filterValue.value = value;
  console.log(filterValue.value, value);
};

/*
Toggle Show Modal
*/
const showModal = ref(false);
const toggleShowModal = () => {
  showModal.value = !showModal.value;
};
/*
Toggle Create Order Modal
*/
const createModal = ref(false);
const toggleCreateModal = () => {
  toggleShowModal();
  createModal.value = !createModal.value;
};
/*
Toggle Edit Order Modal
*/
const editModal = ref(false);
const editOrderId = ref("");
const toggleEditModal = (id) => {
  editOrderId.value = id;
  toggleShowModal();
  editModal.value = !editModal.value;
};

/*
Order Data
*/
const orderList = reactive([
  {
    orderId: "ON1236",
    invoiceId: "1236",
    customerName: "Mr Uzumaki Naruto",
    date: "17/06/2022",
    status: "completed",
  },
  {
    orderId: "ON1275",
    invoiceId: "1275",
    customerName: "Mr Satoshi Nakamoto",
    date: "19/09/2022",
    status: "cancelled",
  },
  {
    orderId: "ON1235",
    invoiceId: "1235",
    customerName: "Mr Ryuuguji Ken",
    date: "16/12/2021",
    status: "cancelled",
  },
  {
    orderId: "ON1233",
    invoiceId: "1233",
    customerName: "Mr Gon Freecs",
    date: "12/03/2022",
    status: "pending",
  },
  {
    orderId: "ON3453",
    invoiceId: "3453",
    customerName: "Mr Killua Zoldyk",
    date: "16/07/2021",
    status: "completed",
  },
  {
    orderId: "ON1723",
    invoiceId: "1723",
    customerName: "Mr Ilumi Zoldyk",
    date: "21/02/2022",
    status: "pending",
  },
  {
    orderId: "ON6123",
    invoiceId: "6123",
    customerName: "Mr Heathcliff",
    date: "16/09/2021",
    status: "completed",
  },
  {
    orderId: "ON1239",
    invoiceId: "1239",
    customerName: "	Mr Akihiko Kayaba",
    date: "19/07/2021",
    status: "cancelled",
  },
  {
    orderId: "ON2768",
    invoiceId: "2768",
    customerName: "Mr Hikigaya Hachiman",
    date: "08/08/2021",
    status: "pending",
  },
  {
    orderId: "ON1723",
    invoiceId: "1723",
    customerName: "	Mr Akashi Seijuro",
    date: "17/06/2020",
    status: "completed",
  },
  {
    orderId: "ON1980",
    invoiceId: "1980",
    customerName: "Mr AJ Raikage",
    date: "11/09/2019",
    status: "completed",
  },
  {
    orderId: "ON1998",
    invoiceId: "1998",
    customerName: "	Mr Kuroko Tetsuya",
    date: "16/07/2020",
    status: "completed",
  },
]);
/*
Increment Index key function
*/
const incrementIndex = (i) => {
  return i + 1;
};
</script>

<style scoped>
.orders-section {
  background: var(--dark-color2);
  padding: 40px 30px;
  width: 100%;
  overflow-y: auto;
  height: calc(100vh - 110px);
}
.orders-section .section-content {
  display: flex;
  flex-direction: column;
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
.add-btn {
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
}
.activity-link + .activity-link {
  margin-left: 25px;
}
.activity-link {
  padding-bottom: 10px;
  position: relative;
  cursor: pointer;
  transition: 0.3s;
}
.activity-link.active {
  color: #bebec4;
  font-weight: 500;
}
.activity-link.active:before {
  content: "";
  position: absolute;
  width: 22px;
  height: 2px;
  background: #4255d4;
  left: 0;
  bottom: 0;
}
/* Order content */
.orders-container {
  margin-top: 20px;
  padding: 0 20px;
  display: block;
  /* max-height: 420px;
  overflow-y: auto; */
}
.orders-container table {
  width: 100%;
  border-collapse: collapse;
}
.orders-container .table-header {
  background-color: #212752;
  position: sticky;
  top: 0;
  z-index: 1;
}
.orders-container th {
  text-align: left;
  padding: 5px;
}
.orders-container td {
  padding: 10px 5px;
}
tr {
  min-height: 50px;
}
/* Status */
.status {
  display: inline-flex;
  align-items: center;
}
.status svg {
  margin-right: 6px;
  width: 22px;
  height: 22px;
  padding: 3px;
  border-radius: 4px;
  color: currentColor;
}
.status-completed {
  color: #1aa385;
}
.status-completed svg {
  background-color: #142940;
}
.status-cancelled {
  color: var(--red-color);
}
.status-cancelled svg {
  background: #2e2142;
}
.status-pending {
  color: #3e4ec2;
}
.status-pending:before {
  width: 22px;
  height: 22px;
  position: absolute;
  left: 0;
  top: 0;
  content: "";
  background: #1a214d;
  border-radius: 4px;
}
.status-pending svg {
  /* background: #2e2142; */
  -webkit-animation: spin 4s linear infinite;
  -moz-animation: spin 4s linear infinite;
  animation: spin 4s linear infinite;
}
/* Option Menu */
.option {
  position: relative;
}
.option-icon {
  color: var(--text-color);
  fill: currentColor;
  cursor: pointer;
}
.option .option-menu {
  position: absolute;
  background: var(--dark-color2);
  padding: 5px 0;
  right: -2px;
  bottom: -2px;
  z-index: 2;
  transform: scale(0);
  border-radius: 5px;
  transform-origin: top right;
  transition: transform 0.2s ease;
  box-shadow: 0 0 6px rgb(0 0 0 / 15%);
}
.option:hover .option-menu {
  transform: scale(1);
}
.option .option-menu .menu-item {
  height: 25px;
  font-size: 16px;
  padding: 15px;
  margin-bottom: 2px;
  color: var(--text-color);
  display: flex;
  align-items: center;
  justify-content: flex-start;
  cursor: pointer;
}

.option .option-menu .menu-item:hover {
  background: var(--dark-color1);
}

@-moz-keyframes spin {
  100% {
    -moz-transform: rotate(360deg);
  }
}
@-webkit-keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
  }
}
@keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
</style>
