<template>
  <div class="invoices-section">
    <div class="section-content">
      <div class="section-header">
        <p>Invoice</p>
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
      <div class="invoices-section-line">
        <div class="invoices-status">
          <div class="item-status">
            <span class="status-number"> 26 </span>
            <span class="status-type"> Total Invoices </span>
          </div>
        </div>
        <div class="view-actions">
          <button class="view-btn list-view" @click="listView">
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
            >
              <line x1="8" y1="6" x2="21" y2="6"></line>
              <line x1="8" y1="12" x2="21" y2="12"></line>
              <line x1="8" y1="18" x2="21" y2="18"></line>
              <line x1="3" y1="6" x2="3.01" y2="6"></line>
              <line x1="3" y1="12" x2="3.01" y2="12"></line>
              <line x1="3" y1="18" x2="3.01" y2="18"></line>
            </svg>
          </button>
          <button class="view-btn grid-view active" @click="gridView">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <rect x="3" y="3" width="7" height="7"></rect>
              <rect x="14" y="3" width="7" height="7"></rect>
              <rect x="14" y="14" width="7" height="7"></rect>
              <rect x="3" y="14" width="7" height="7"></rect>
            </svg>
          </button>
        </div>
      </div>
      <div class="invoices-container grid-view">
        <div class="item-wrapper">
          <div class="invoice-item">
            <div class="item-header">
              <span class="item-id"> 1239 </span>
              <button class="view-btn">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 576 512"
                  width="24"
                  height="24"
                  fill="currentColor"
                  stroke="currentColor"
                >
                  <path
                    d="M279.6 160.4C282.4 160.1 285.2 160 288 160C341 160 384 202.1 384 256C384 309 341 352 288 352C234.1 352 192 309 192 256C192 253.2 192.1 250.4 192.4 247.6C201.7 252.1 212.5 256 224 256C259.3 256 288 227.3 288 192C288 180.5 284.1 169.7 279.6 160.4zM480.6 112.6C527.4 156 558.7 207.1 573.5 243.7C576.8 251.6 576.8 260.4 573.5 268.3C558.7 304 527.4 355.1 480.6 399.4C433.5 443.2 368.8 480 288 480C207.2 480 142.5 443.2 95.42 399.4C48.62 355.1 17.34 304 2.461 268.3C-.8205 260.4-.8205 251.6 2.461 243.7C17.34 207.1 48.62 156 95.42 112.6C142.5 68.84 207.2 32 288 32C368.8 32 433.5 68.84 480.6 112.6V112.6zM288 112C208.5 112 144 176.5 144 256C144 335.5 208.5 400 288 400C367.5 400 432 335.5 432 256C432 176.5 367.5 112 288 112z"
                  />
                </svg>
              </button>
            </div>
            <div class="item-content">
              <div class="item-details">
                <p>Billed To: Mr Killua Zoldyk</p>
                <p>Customer E-mail: killua@gmail.com</p>
              </div>
              <div class="item-footer">
                <p>Date of Issue: 23/03/2022</p>
              </div>
            </div>
          </div>
        </div>
        <div class="item-wrapper">
          <div class="invoice-item">
            <div class="item-header">
              <span class="item-id"> 1238 </span>
              <button class="view-btn">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 576 512"
                  width="24"
                  height="24"
                  fill="currentColor"
                  stroke="currentColor"
                >
                  <path
                    d="M279.6 160.4C282.4 160.1 285.2 160 288 160C341 160 384 202.1 384 256C384 309 341 352 288 352C234.1 352 192 309 192 256C192 253.2 192.1 250.4 192.4 247.6C201.7 252.1 212.5 256 224 256C259.3 256 288 227.3 288 192C288 180.5 284.1 169.7 279.6 160.4zM480.6 112.6C527.4 156 558.7 207.1 573.5 243.7C576.8 251.6 576.8 260.4 573.5 268.3C558.7 304 527.4 355.1 480.6 399.4C433.5 443.2 368.8 480 288 480C207.2 480 142.5 443.2 95.42 399.4C48.62 355.1 17.34 304 2.461 268.3C-.8205 260.4-.8205 251.6 2.461 243.7C17.34 207.1 48.62 156 95.42 112.6C142.5 68.84 207.2 32 288 32C368.8 32 433.5 68.84 480.6 112.6V112.6zM288 112C208.5 112 144 176.5 144 256C144 335.5 208.5 400 288 400C367.5 400 432 335.5 432 256C432 176.5 367.5 112 288 112z"
                  />
                </svg>
              </button>
            </div>
            <div class="item-content">
              <div class="item-details">
                <p>Billed To: Mr Naruto Uzumaki</p>
                <p>Customer E-mail: narutohina@gmail.com</p>
              </div>
              <div class="item-footer">
                <p>Date of Issue: 27/03/2022</p>
              </div>
            </div>
          </div>
        </div>
        <div class="item-wrapper">
          <div class="invoice-item">
            <div class="item-header">
              <span class="item-id"> 1237 </span>
              <button class="view-btn">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 576 512"
                  width="24"
                  height="24"
                  fill="currentColor"
                  stroke="currentColor"
                >
                  <path
                    d="M279.6 160.4C282.4 160.1 285.2 160 288 160C341 160 384 202.1 384 256C384 309 341 352 288 352C234.1 352 192 309 192 256C192 253.2 192.1 250.4 192.4 247.6C201.7 252.1 212.5 256 224 256C259.3 256 288 227.3 288 192C288 180.5 284.1 169.7 279.6 160.4zM480.6 112.6C527.4 156 558.7 207.1 573.5 243.7C576.8 251.6 576.8 260.4 573.5 268.3C558.7 304 527.4 355.1 480.6 399.4C433.5 443.2 368.8 480 288 480C207.2 480 142.5 443.2 95.42 399.4C48.62 355.1 17.34 304 2.461 268.3C-.8205 260.4-.8205 251.6 2.461 243.7C17.34 207.1 48.62 156 95.42 112.6C142.5 68.84 207.2 32 288 32C368.8 32 433.5 68.84 480.6 112.6V112.6zM288 112C208.5 112 144 176.5 144 256C144 335.5 208.5 400 288 400C367.5 400 432 335.5 432 256C432 176.5 367.5 112 288 112z"
                  />
                </svg>
              </button>
            </div>
            <div class="item-content">
              <div class="item-details">
                <p>Billed To: Mr AJ Raikage</p>
                <p>Customer E-mail: ajraikage2@gmail.com</p>
              </div>
              <div class="item-footer">
                <p>Date of Issue: 29/03/2022</p>
              </div>
            </div>
          </div>
        </div>
        <div class="item-wrapper">
          <div class="invoice-item">
            <div class="item-header">
              <span class="item-id"> 1236 </span>
              <button class="view-btn">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 576 512"
                  width="24"
                  height="24"
                  fill="currentColor"
                  stroke="currentColor"
                >
                  <path
                    d="M279.6 160.4C282.4 160.1 285.2 160 288 160C341 160 384 202.1 384 256C384 309 341 352 288 352C234.1 352 192 309 192 256C192 253.2 192.1 250.4 192.4 247.6C201.7 252.1 212.5 256 224 256C259.3 256 288 227.3 288 192C288 180.5 284.1 169.7 279.6 160.4zM480.6 112.6C527.4 156 558.7 207.1 573.5 243.7C576.8 251.6 576.8 260.4 573.5 268.3C558.7 304 527.4 355.1 480.6 399.4C433.5 443.2 368.8 480 288 480C207.2 480 142.5 443.2 95.42 399.4C48.62 355.1 17.34 304 2.461 268.3C-.8205 260.4-.8205 251.6 2.461 243.7C17.34 207.1 48.62 156 95.42 112.6C142.5 68.84 207.2 32 288 32C368.8 32 433.5 68.84 480.6 112.6V112.6zM288 112C208.5 112 144 176.5 144 256C144 335.5 208.5 400 288 400C367.5 400 432 335.5 432 256C432 176.5 367.5 112 288 112z"
                  />
                </svg>
              </button>
            </div>
            <div class="item-content">
              <div class="item-details">
                <p>Billed To: Mr Ryuuguji Ken</p>
                <p>Customer E-mail: draken@gmail.com</p>
              </div>
              <div class="item-footer">
                <p>Date of Issue: 28/04/2022</p>
              </div>
            </div>
          </div>
        </div>
        <div class="item-wrapper">
          <div class="invoice-item">
            <div class="item-header">
              <span class="item-id"> 1235 </span>
              <button class="view-btn">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 576 512"
                  width="24"
                  height="24"
                  fill="currentColor"
                  stroke="currentColor"
                >
                  <path
                    d="M279.6 160.4C282.4 160.1 285.2 160 288 160C341 160 384 202.1 384 256C384 309 341 352 288 352C234.1 352 192 309 192 256C192 253.2 192.1 250.4 192.4 247.6C201.7 252.1 212.5 256 224 256C259.3 256 288 227.3 288 192C288 180.5 284.1 169.7 279.6 160.4zM480.6 112.6C527.4 156 558.7 207.1 573.5 243.7C576.8 251.6 576.8 260.4 573.5 268.3C558.7 304 527.4 355.1 480.6 399.4C433.5 443.2 368.8 480 288 480C207.2 480 142.5 443.2 95.42 399.4C48.62 355.1 17.34 304 2.461 268.3C-.8205 260.4-.8205 251.6 2.461 243.7C17.34 207.1 48.62 156 95.42 112.6C142.5 68.84 207.2 32 288 32C368.8 32 433.5 68.84 480.6 112.6V112.6zM288 112C208.5 112 144 176.5 144 256C144 335.5 208.5 400 288 400C367.5 400 432 335.5 432 256C432 176.5 367.5 112 288 112z"
                  />
                </svg>
              </button>
            </div>
            <div class="item-content">
              <div class="item-details">
                <p>Billed To: Mr Satoshi Nakamoto</p>
                <p>Customer E-mail: bitcoin@gmail.com</p>
              </div>
              <div class="item-footer">
                <p>Date of Issue: 26/02/2022</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive, onMounted } from "vue";
const listView = () => {
  document.querySelector(".list-view").classList.add("active");
  document.querySelector(".grid-view").classList.remove("active");
  document.querySelector(".invoices-container").classList.add("list-view");
  document.querySelector(".invoices-container").classList.remove("grid-view");
};
const gridView = () => {
  document.querySelector(".list-view").classList.remove("active");
  document.querySelector(".grid-view").classList.add("active");
  document.querySelector(".invoices-container").classList.add("grid-view");
  document.querySelector(".invoices-container").classList.remove("list-view");
};
</script>

<style scoped>
.invoices-section {
  background: var(--dark-color2);
  padding: 40px 30px;
  width: 100%;
  overflow: hidden;
  border-radius: 32px;
}
.invoices-section .section-content {
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
/* Invoice Section Line */
.invoices-section-line {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 30px 0;
}
.invoices-status {
  padding-left: 20px;
}
.item-status {
  display: flex;
  flex-direction: column;
}
.status-number {
  font-size: 24px;
  line-height: 32px;
  font-weight: 700;
}
.status-type {
  position: relative;
  padding-right: 24px;
  color: #4a4a4a;
}
.view-actions {
  display: flex;
  align-items: center;
}
.view-btn {
  width: 36px;
  height: 36px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 6px;
  border-radius: 4px;
  background-color: transparent;
  border: none;
  color: var(--text-color);
  margin-left: 8px;
  transition: 0.2s;
}
.view-btn.active {
  background-color: var(--dark-color1);
  color: #fff;
}

/* Invoices container */
.invoices-container {
  padding: 0 20px;
  display: block;
  max-height: 420px;
  overflow-y: auto;
}
.item-wrapper {
  padding: 8px;
  transition: 0.2s;
}
/* Grid-View */
.invoices-container.grid-view {
  display: flex;
  flex-wrap: wrap;
}
.invoices-container.grid-view .item-wrapper {
  width: 33.3%;
}
.invoices-container.grid-view .invoice-item {
    min-height: 200px;
}
/* List- View */
.invoices-container.list-view .invoice-item {
  border-radius: 10px;
}
.invoices-container.list-view .item-details {
  text-align: left;
}
.invoices-container.list-view .item-details p {
  display: inline-block;
  margin-right: 15px;
}
.invoices-container.list-view .item-header {
  margin-bottom: 8px;
}
.invoices-container.list-view .item-details {
  margin-bottom: 8px;
}
.invoices-container.list-view .item-footer {
  margin-top: 8px;
}
.invoice-item {
  border-radius: 30px;
  padding: 16px;
  background: radial-gradient(circle, #1a2049 0%, #13162f 100%);
}
.invoice-item .item-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 18px;
}
.item-header .item-id {
  opacity: 0.8;
  font-size: 20px;
  line-height: 16px;
}
.item-header .view-btn {
  padding: 0;
  width: 24px;
  height: 24px;
  position: relative;
  background-color: transparent;
  border: none;
  cursor: pointer;
}
.item-content .item-details {
  text-align: center;
  margin-bottom: 18px;
}
.item-content .item-details p {
  color: #fff;
  font-size: 16px;
  line-height: 24px;
  font-weight: 600;
  opacity: 0.8;
}
.item-content .item-footer {
  margin-top: 18px;
}
</style>
