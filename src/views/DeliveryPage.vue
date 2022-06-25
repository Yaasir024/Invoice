<template>
  <div class="delivery-section">
    <div class="section-content">
      <div class="section-header">
        <p>Delivery</p>
        <div class="search-box">
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
          <div class="select-filter">
            <select class="select">
              <option value="0">Filter</option>
              <option value="1">Filter by Number</option>
              <option value="2">Filter by Destination</option>
            </select>
          </div>
        </div>
        <button class="settings-btn">
          <svg
            viewBox="0 0 512 512"
            fill="currentColor"
            class="btn-icon"
            width="18"
            height="18"
          >
            <path
              d="M272 512h-32c-26 0-47.2-21.1-47.2-47.1V454c-11-3.5-21.8-8-32.1-13.3l-7.7 7.7a47.1 47.1 0 01-66.7 0l-22.7-22.7a47.1 47.1 0 010-66.7l7.7-7.7c-5.3-10.3-9.8-21-13.3-32.1H47.1c-26 0-47.1-21.1-47.1-47.1v-32.2c0-26 21.1-47.1 47.1-47.1H58c3.5-11 8-21.8 13.3-32.1l-7.7-7.7a47.1 47.1 0 010-66.7l22.7-22.7a47.1 47.1 0 0166.7 0l7.7 7.7c10.3-5.3 21-9.8 32.1-13.3V47.1c0-26 21.1-47.1 47.1-47.1h32.2c26 0 47.1 21.1 47.1 47.1V58c11 3.5 21.8 8 32.1 13.3l7.7-7.7a47.1 47.1 0 0166.7 0l22.7 22.7a47.1 47.1 0 010 66.7l-7.7 7.7c5.3 10.3 9.8 21 13.3 32.1h10.9c26 0 47.1 21.1 47.1 47.1v32.2c0 26-21.1 47.1-47.1 47.1H454c-3.5 11-8 21.8-13.3 32.1l7.7 7.7a47.1 47.1 0 010 66.7l-22.7 22.7a47.1 47.1 0 01-66.7 0l-7.7-7.7c-10.3 5.3-21 9.8-32.1 13.3v10.9c0 26-21.1 47.1-47.1 47.1zM165.8 409.2a176.8 176.8 0 0045.8 19 15 15 0 0111.3 14.5V465c0 9.4 7.7 17.1 17.1 17.1h32.2c9.4 0 17.1-7.7 17.1-17.1v-22.2a15 15 0 0111.3-14.5c16-4.2 31.5-10.6 45.8-19a15 15 0 0118.2 2.3l15.7 15.7a17.1 17.1 0 0024.2 0l22.8-22.8a17.1 17.1 0 000-24.2l-15.7-15.7a15 15 0 01-2.3-18.2 176.8 176.8 0 0019-45.8 15 15 0 0114.5-11.3H465c9.4 0 17.1-7.7 17.1-17.1v-32.2c0-9.4-7.7-17.1-17.1-17.1h-22.2a15 15 0 01-14.5-11.2c-4.2-16.1-10.6-31.6-19-45.9a15 15 0 012.3-18.2l15.7-15.7a17.1 17.1 0 000-24.2l-22.8-22.8a17.1 17.1 0 00-24.2 0l-15.7 15.7a15 15 0 01-18.2 2.3 176.8 176.8 0 00-45.8-19 15 15 0 01-11.3-14.5V47c0-9.4-7.7-17.1-17.1-17.1h-32.2c-9.4 0-17.1 7.7-17.1 17.1v22.2a15 15 0 01-11.3 14.5c-16 4.2-31.5 10.6-45.8 19a15 15 0 01-18.2-2.3l-15.7-15.7a17.1 17.1 0 00-24.2 0l-22.8 22.8a17.1 17.1 0 000 24.2l15.7 15.7a15 15 0 012.3 18.2 176.8 176.8 0 00-19 45.8 15 15 0 01-14.5 11.3H47c-9.4 0-17.1 7.7-17.1 17.1v32.2c0 9.4 7.7 17.1 17.1 17.1h22.2a15 15 0 0114.5 11.3c4.2 16 10.6 31.5 19 45.8a15 15 0 01-2.3 18.2l-15.7 15.7a17.1 17.1 0 000 24.2l22.8 22.8a17.1 17.1 0 0024.2 0l15.7-15.7a15 15 0 0118.2-2.3z"
              data-v-61dd7a3d=""
            ></path>
            <path
              d="M256 367.4c-61.4 0-111.4-50-111.4-111.4s50-111.4 111.4-111.4 111.4 50 111.4 111.4-50 111.4-111.4 111.4zm0-192.8a81.5 81.5 0 000 162.8 81.5 81.5 0 000-162.8z"
              data-v-61dd7a3d=""
            ></path>
          </svg>
        </button>
      </div>
      <!-- Activity Link -->
      <div class="activity-links">
        <div class="activity-link active">All</div>
        <div class="activity-link">Completed</div>
        <div class="activity-link">Pending</div>
        <div class="activity-link">Cancelled</div>
      </div>
      <!-- Deliveries container -->
      <div class="deliveries-container">
        <table class="table">
          <tr class="table-header">
            <th></th>
            <th>No</th>
            <th>Delivery Number</th>
            <th>Invoice Id</th>
            <th>Destination</th>
            <th>Delivery Date</th>
            <th>Status</th>
            <th></th>
          </tr>
          <tr>
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td>11</td>
            <td>DN00000003</td>
            <td>3721</td>
            <td>Konoha</td>
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
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td>09</td>
            <td>DN00000005</td>
            <td>3321</td>
            <td>Konoha</td>
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
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td>10</td>
            <td>DN00000004</td>
            <td>3761</td>
            <td>Jibuti</td>
            <td>17/07/2022</td>
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
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td>11</td>
            <td>DN00000003</td>
            <td>3721</td>
            <td>Konoha</td>
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
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td>12</td>
            <td>DN00000002</td>
            <td>3711</td>
            <td>Oosaka,Japan</td>
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
            <td class="check">
              <input type="checkbox" name="" id="" />
            </td>
            <td>13</td>
            <td>DN00000001</td>
            <td>3621</td>
            <td>Shibuya</td>
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
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.delivery-section {
  background: var(--dark-color2);
  padding: 30px 30px;
  width: 100%;
  overflow: hidden;
  border-radius: 32px;
}
.delivery-section .section-content {
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
.search-box {
  display: flex;
  align-items: center;
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
/* Filter */
.select-filter {
  margin-left: 10px;
}
select {
  height: 32px;
  color: var(--text-color);
  background: #212752;
  border: none;
  cursor: pointer;
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
  margin-top: 32px;
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
/* Deliveries content */
.deliveries-container {
  margin-top: 20px;
  padding: 0 20px;
  display: block;
  max-height: 420px;
  overflow-y: auto;
}
.deliveries-container table {
  width: 100%;
  border-collapse: collapse;
}
.deliveries-container .table-header {
  background-color: #212752;
  position: sticky;
  top: 0;
  z-index: 1;
}
.deliveries-container th {
  text-align: left;
  padding: 5px;
}
.deliveries-container td {
  padding: 10px 5px;
}
tr {
  min-height: 50px;
}
.check {
  text-align: center;
}
.check input {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  width: 16px;
  height: 16px;
  border: 1px solid #9b9ca7;
  vertical-align: middle;
  background-color: transparent;
  border-radius: 4px;
  cursor: pointer;
  margin-right: 16px;
  transition: 0.25s;
  background-size: 0;
  background-position: center;
}
.check input:checked {
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' width='24' height='24' stroke='%23fff' stroke-width='2' fill='none' stroke-linecap='round' stroke-linejoin='round' class='css-i6dzq1'%3E%3Cpolyline points='20 6 9 17 4 12'%3E%3C/polyline%3E%3C/svg%3E");
    background-color: #252954;
    background-size: 12px;
    background-repeat: no-repeat;
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
