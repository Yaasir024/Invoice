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
        <button class="add-btn">
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
      <div class="activity-link active">All</div>
      <div class="activity-link">Completed</div>
      <div class="activity-link">Pending</div>
      <div class="activity-link">Cancelled</div>
    </div>
    <!-- Orders container -->
    <div class="orders-container">
      <table class="table">
        <tr class="table-header">
          <th>Id</th>
          <th>Invoice Id</th>
          <th>Name</th>
          <th>Date Issued</th>
          <th>Status</th>
          <th></th>
        </tr>
        <tr>
          <td>1</td>
          <td>1236</td>
          <td>
            <span>Mr Uzumaki Naruto</span>
          </td>
          <td>17/06/2022</td>
          <td>
            <div class="status status-completed">
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
          </td>
          <td>
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
          </td>
        </tr>
        <tr>
          <td>2</td>
          <td>1275</td>
          <td>Mr Satoshi Nakamoto</td>
          <td>19/09/2022</td>
          <td>
            <div class="status status-cancelled">
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
          </td>
        </tr>
        <tr>
          <td>3</td>
          <td>1235</td>
          <td>Mr Ryuuguji Ken</td>
          <td>16/12/2021</td>
          <td>
            <div class="status status-pending">
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
          </td>
          <td>
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
          </td>
        </tr>
        <tr>
          <td>4</td>
          <td>1233</td>
          <td>
            <span>Mr Gon Freecs</span>
          </td>
          <td>12/03/2022</td>
          <td>
            <div class="status status-completed">
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
          </td>
          <td>
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
          </td>
        </tr>
        <tr>
          <td>5</td>
          <td>3453</td>
          <td>Mr Killua Zoldyk</td>
          <td>16/07/2021</td>
          <td>
            <div class="status status-cancelled">
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
          </td>
        </tr>
        <tr>
          <td>6</td>
          <td>1723</td>
          <td>Mr Ilumi Zoldyk</td>
          <td>21/02/2022</td>
          <td>
            <div class="status status-pending">
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
          </td>
          <td>
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
          </td>
        </tr>
        <tr>
          <td>7</td>
          <td>6123</td>
          <td>
            <span>Mr Heathcliff</span>
          </td>
          <td>16/09/2021</td>
          <td>
            <div class="status status-completed">
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
          </td>
          <td>
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
          </td>
        </tr>
        <tr>
          <td>8</td>
          <td>1239</td>
          <td>Mr Akihiko Kayaba</td>
          <td>19/07/2021</td>
          <td>
            <div class="status status-cancelled">
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
          </td>
        </tr>
        <tr>
          <td>9</td>
          <td>2768</td>
          <td>Mr Hikigaya Hachiman</td>
          <td>8/08/2021</td>
          <td>
            <div class="status status-pending">
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
          </td>
          <td>
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
          </td>
        </tr>
        <tr>
          <td>10</td>
          <td>1723</td>
          <td>
            <span>Mr Akashi Seijuro</span>
          </td>
          <td>17/06/2022</td>
          <td>
            <div class="status status-completed">
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
          </td>
          <td>
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
          </td>
        </tr>
        <tr>
          <td>11</td>
          <td>1980</td>
          <td>Mr AJ Raikage</td>
          <td>11/09/2019</td>
          <td>
            <div class="status status-cancelled">
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
          </td>
        </tr>
        <tr>
          <td>12</td>
          <td>1998</td>
          <td>Mr Kuroko Tetsuya</td>
          <td>16/07/2022</td>
          <td>
            <div class="status status-pending">
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
          </td>
          <td>
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
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.orders-section {
  background: var(--dark-color2);
  padding: 40px 30px;
  width: 100%;
  overflow: hidden;
  border-radius: 32px;
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
  max-height: 420px;
  overflow-y: auto;
}
.option-icon {
  color: var(--text-color);
  fill: currentColor;
  cursor: pointer;
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
  -webkit-animation:spin 4s linear infinite;
    -moz-animation:spin 4s linear infinite;
    animation:spin 4s linear infinite;
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
