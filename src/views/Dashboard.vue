<script setup>
// import TheWelcome from '@/components/TheWelcome.vue'
</script>

<template>
  <main class="dashboard-section">
    <div class="dashboard-content">
      <div class="section-header">
        <p class="section-title">Dashboard</p>
        <div class="total-container">
          <div class="total-box total-sales">
            <div class="icon">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 320 512"
                width="20"
                height="20"
              >
                <path
                  d="M160 0C177.7 0 192 14.33 192 32V67.68C193.6 67.89 195.1 68.12 196.7 68.35C207.3 69.93 238.9 75.02 251.9 78.31C268.1 82.65 279.4 100.1 275 117.2C270.7 134.3 253.3 144.7 236.1 140.4C226.8 137.1 198.5 133.3 187.3 131.7C155.2 126.9 127.7 129.3 108.8 136.5C90.52 143.5 82.93 153.4 80.92 164.5C78.98 175.2 80.45 181.3 82.21 185.1C84.1 189.1 87.79 193.6 95.14 198.5C111.4 209.2 136.2 216.4 168.4 225.1L171.2 225.9C199.6 233.6 234.4 243.1 260.2 260.2C274.3 269.6 287.6 282.3 295.8 299.9C304.1 317.7 305.9 337.7 302.1 358.1C295.1 397 268.1 422.4 236.4 435.6C222.8 441.2 207.8 444.8 192 446.6V480C192 497.7 177.7 512 160 512C142.3 512 128 497.7 128 480V445.1C127.6 445.1 127.1 444.1 126.7 444.9L126.5 444.9C102.2 441.1 62.07 430.6 35 418.6C18.85 411.4 11.58 392.5 18.76 376.3C25.94 360.2 44.85 352.9 60.1 360.1C81.9 369.4 116.3 378.5 136.2 381.6C168.2 386.4 194.5 383.6 212.3 376.4C229.2 369.5 236.9 359.5 239.1 347.5C241 336.8 239.6 330.7 237.8 326.9C235.9 322.9 232.2 318.4 224.9 313.5C208.6 302.8 183.8 295.6 151.6 286.9L148.8 286.1C120.4 278.4 85.58 268.9 59.76 251.8C45.65 242.4 32.43 229.7 24.22 212.1C15.89 194.3 14.08 174.3 17.95 153C25.03 114.1 53.05 89.29 85.96 76.73C98.98 71.76 113.1 68.49 128 66.73V32C128 14.33 142.3 0 160 0V0z"
                />
              </svg>
            </div>
            <div class="total-details">
              <p class="total-title">Total Sales</p>
              <p class="total-value">$200,000,056</p>
            </div>
          </div>
          <div class="total-box total-sales">
            <div class="icon">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 576 512"
                fill="currentColor"
                width="20"
                height="20"
              >
                <path
                  d="M96 0C107.5 0 117.4 8.19 119.6 19.51L121.1 32H541.8C562.1 32 578.3 52.25 572.6 72.66L518.6 264.7C514.7 278.5 502.1 288 487.8 288H170.7L179.9 336H488C501.3 336 512 346.7 512 360C512 373.3 501.3 384 488 384H159.1C148.5 384 138.6 375.8 136.4 364.5L76.14 48H24C10.75 48 0 37.25 0 24C0 10.75 10.75 0 24 0H96zM128 464C128 437.5 149.5 416 176 416C202.5 416 224 437.5 224 464C224 490.5 202.5 512 176 512C149.5 512 128 490.5 128 464zM512 464C512 490.5 490.5 512 464 512C437.5 512 416 490.5 416 464C416 437.5 437.5 416 464 416C490.5 416 512 437.5 512 464z"
                  data-v-65af85a3=""
                ></path>
              </svg>
            </div>
            <div class="total-details">
              <p class="total-title">Total Orders</p>
              <p class="total-value">200</p>
            </div>
          </div>
          <div class="total-box total-sales">
            <div class="icon">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 448 512"
                fill="currentColor"
                width="20"
                height="20"
              >
                <path
                  d="M112 112C112 50.14 162.1 0 224 0C285.9 0 336 50.14 336 112V160H400C426.5 160 448 181.5 448 208V416C448 469 405 512 352 512H96C42.98 512 0 469 0 416V208C0 181.5 21.49 160 48 160H112V112zM160 160H288V112C288 76.65 259.3 48 224 48C188.7 48 160 76.65 160 112V160zM136 256C149.3 256 160 245.3 160 232C160 218.7 149.3 208 136 208C122.7 208 112 218.7 112 232C112 245.3 122.7 256 136 256zM312 208C298.7 208 288 218.7 288 232C288 245.3 298.7 256 312 256C325.3 256 336 245.3 336 232C336 218.7 325.3 208 312 208z"
                  data-v-65af85a3=""
                ></path>
              </svg>
            </div>
            <div class="total-details">
              <p class="total-title">Total Products</p>
              <p class="total-value">56</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
.dashboard-section {
  background: var(--dark-color2);
  padding: 30px 30px;
  width: 100%;
  overflow: hidden;
  border-radius: 32px;
}
.dashboard-content {
  overflow-y: auto;
  max-height: 560px;
}
.section-header .section-title {
  font-size: 24px;
  font-weight: 700;
  opacity: 0.9;
}
.total-container {
  display: flex;
  align-items: center;
  margin-top: 5px;
}
.total-box {
  display: flex;
  align-items: center;
  background: #212752;
  border-radius: 5px;
  margin-right: 20px;
  padding: 20px 15px;
  width: 33.3333%;
}
.icon {
  color: #fff;
  margin-right: 20px;
  background-color: var(--feature-color);
  box-shadow: 0 0 0 7px rgba(66, 85, 212, 0.508);
  padding: 0;
  border: 0;
  border-radius: 50%;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
}
.icon svg {
  fill: currentColor;
}
.total-details .total-title {
  font-weight: 700;
}
.total-details .total-value {
  color: #fff;
  font-weight: 600;
}
</style>
