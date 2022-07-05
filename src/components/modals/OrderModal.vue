<template>
  <div class="modal-wrap" :class="showModal ? 'show' : 'hide'">
    <form @submit.prevent="submitForm" class="modal-content">
      <h1>New Invoice</h1>

      <!-- Bill From -->
      <div class="bill-from flex flex-column">
        <h4>Bill From</h4>
        <div class="input flex flex-column">
          <label for="billerStreetAddress">Street Address</label>
          <input
            required
            type="text"
            id="billerStreetAddress"
            v-model="invoiceData.billerStreetAddress"
          />
        </div>
        <div class="location-details flex">
          <div class="input flex flex-column">
            <label for="billerCity">City</label>
            <input
              required
              type="text"
              id="billerCity"
              v-model="invoiceData.billerCity"
            />
          </div>
          <div class="input flex flex-column">
            <label for="billerZipCode">Zip Code</label>
            <input
              required
              type="text"
              id="billerZipCode"
              v-model="invoiceData.billerZipCode"
            />
          </div>
          <div class="input flex flex-column">
            <label for="billerCountry">Country</label>
            <input
              required
              type="text"
              id="billerCountry"
              v-model="invoiceData.billerCountry"
            />
          </div>
        </div>
      </div>
      <!-- Bill To -->
      <div class="bill-to flex flex-column">
        <h4>Bill To</h4>
        <div class="input flex flex-column">
          <label for="clientName">Client's Name</label>
          <input
            required
            type="text"
            id="clientName"
            v-model="invoiceData.clientName"
          />
        </div>
        <div class="input flex flex-column">
          <label for="clientEmail">Client's Email</label>
          <input
            required
            type="text"
            id="clientEmail"
            v-model="invoiceData.clientEmail"
          />
        </div>
        <div class="input flex flex-column">
          <label for="clientStreetAddress">Street Address</label>
          <input
            required
            type="text"
            id="clientStreetAddress"
            v-model="invoiceData.clientStreetAddress"
          />
        </div>
        <div class="location-details flex">
          <div class="input flex flex-column">
            <label for="clientCity">City</label>
            <input
              required
              type="text"
              id="clientCity"
              v-model="invoiceData.clientCity"
            />
          </div>
          <div class="input flex flex-column">
            <label for="clientZipCode">Zip Code</label>
            <input
              required
              type="text"
              id="clientZipCode"
              v-model="invoiceData.clientZipCode"
            />
          </div>
          <div class="input flex flex-column">
            <label for="clientCountry">Country</label>
            <input
              required
              type="text"
              id="clientCountry"
              v-model="invoiceData.clientCountry"
            />
          </div>
        </div>
      </div>
      <!-- Invoice Work Details -->
      <div class="invoice-work flex flex-column">
        <div class="payment flex">
          <div class="input flex flex-column">
            <label for="invoiceDate">Invoice Date</label>
            <input
              disabled
              type="text"
              id="invoiceDate"
              v-model="invoiceData.invoiceDate"
            />
          </div>
          <div class="input flex flex-column">
            <label for="paymentDueDate">Payment Due</label>
            <input
              disabled
              type="text"
              id="paymentDueDate"
              v-model="invoiceData.paymentDueDate"
            />
          </div>
        </div>
        <div class="input flex flex-column">
          <label for="paymentTerms">Payment Terms</label>
          <select
            required
            type="text"
            id="paymentTerms"
            v-model="invoiceData.paymentTerms"
          >
            <option value="30">Net 30 Days</option>
            <option value="60">Net 60 Days</option>
          </select>
        </div>
        <div class="input flex flex-column">
          <label for="productDescription">Product Description</label>
          <input
            required
            type="text"
            id="productDescription"
            v-model="invoiceData.productDescription"
          />
        </div>
        <div class="work-items">
          <h3>Item List</h3>
          <table class="item-list">
            <tr class="table-heading flex">
              <th class="item-name">Item Name</th>
              <th class="qty">Qty</th>
              <th class="price">Price</th>
              <th class="total">Total</th>
            </tr>
            <tr
              class="table-items flex"
              v-for="(item, index) in invoiceData.invoiceItemList"
              :key="index"
            >
              <td class="item-name">
                <input type="text" v-model="invoiceData.item.itemName" />
              </td>
              <td class="qty">
                <input type="text" v-model="invoiceData.item.qty" />
              </td>
              <td class="price">
                <input type="text" v-model="invoiceData.item.price" />
              </td>
              <td class="total flex">
                ${{
                  (invoiceData.item.total =
                    invoiceData.item.qty * invoiceData.item.price)
                }}
              </td>
              <p @click="deleteInvoiceItem(invoiceData.item.id)">Delete</p>
              <!-- <img
                  @click="deleteInvoiceItem(invoiceData.item.id)"
                  src="@/assets/icon-delete.svg"
                  alt=""
                /> -->
            </tr>
          </table>

          <div @click="addNewInvoiceItem" class="flex add-button">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="14"
              height="14"
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
            Add New Item
          </div>
        </div>
      </div>
      <!-- Buttons Section -->
      <div class="btn-section flex">
        <div class="left">
          <button type="button" class="btn red" @click="$emit('closeCreateModal')">Cancel</button>
        </div>
        <div class="right flex">
          <button type="button" class="btn blue">Save Draft</button>
          <button type="button" class="btn green">Create Invoice</button>
        </div>
      </div>
    </form>
    <div class="create-modal"></div>
    <div class="edit-modal" v-if="editModal"></div>
  </div>
</template>

<script setup>
/*
  imports
  */
import { ref, reactive } from "vue";

const props = defineProps([
  "showModal",
  "createModal",
  "editModal",
  "editOrderId",
]);
const emit = defineEmits(["closeCreateModal", "closeEditModal"]);
const loading = ref(false);
const invoiceData = reactive({
  docId: null,
  billerStreetAddress: null,
  billerCity: null,
  billerZipCode: null,
  billerCountry: null,
  clientName: null,
  clientEmail: null,
  clientStreetAddress: null,
  clientCity: null,
  clientZipCode: null,
  clientCountry: null,
  invoiceDateUnix: null,
  invoiceDate: null,
  paymentTerms: null,
  paymentDueDateUnix: null,
  paymentDueDate: null,
  productDescription: null,
  invoicePending: null,
  invoiceDraft: null,
  invoiceItemList: [],
  invoiceTotal: 0,
});
</script>

<style scoped>
/* Basic */
.flex {
  display: flex;
}
.flex-column {
  flex-direction: column;
}
.modal-wrap {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  transition: all 0.32s ease-in-out;
  z-index: 5;
  overflow-y: auto;
}
.modal-content {
  position: relative;
  padding: 56px;
  max-width: 700px;
  width: 100%;
  background: var(--dark-color1);
}
.modal-content h1 {
  margin-bottom: 48px;
}
.modal-content h3 {
  margin-bottom: 16px;
  font-size: 18px;
}
.modal-content h4 {
  font-size: 12px;
  margin-bottom: 24px;
}
/* Bill to & Bill From */
.bill-to,
.bill-from {
  margin-bottom: 48px;
}
.location-details {
  gap: 16px;
}
.location-details div {
  flex: 1;
}
/* Invoice Work */
.invoice-work .payment {
  gap: 24px;
}
.invoice-work .payment div {
  flex: 1;
}
.work-items .item-list {
  width: 100%;
}
/* Item Table Styling */
.table-heading,
.table-items {
  gap: 16px;
  font-size: 12px;
}
.item-name {
  flex-basis: 50%;
}
.qty {
  flex-basis: 10%;
}
.price {
  flex-basis: 20%;
}
.total {
  flex-basis: 20%;
  align-self: center;
}
.table-heading {
  margin-bottom: 16px;
}
.table-heading th {
  text-align: left;
}
.add-button {
  color: var(--light-color);
  cursor: pointer;
  background-color: #212752;
  padding: 8px 10px;
  border-radius: 40px;
  align-items: center;
  justify-content: center;
  width: 100%;
}
.add-button svg {
  margin-right: 4px;
}
.btn-section {
  margin-top: 60px;
}
.btn-section div {
  flex: 1;
}
.btn-section .right {
  justify-content: flex-end;
}
.btn {
  color: var(--light-color);
  cursor: pointer;
  background-color: #212752;

  padding: 14px 18px;
  border-radius: 40px;
  border: none;
}
.blue {
  background-color: var(--dark-color2);
  margin-right: 8px;
}
.red {
  background-color: var(--red-color);
}
.green {
  background-color: var(--green-color);
}
.input {
  margin-bottom: 24px;
}
label {
  font-size: 12px;
  margin-bottom: 6px;
}
input,
select {
  width: 100%;
  color: var(--light-color);
  background-color: var(--dark-color3);
  border-radius: 4px;
  padding: 12px 4px;
  border: none;
}
</style>
