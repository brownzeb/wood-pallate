<template>
  <div>
    <div class="grid-container">
      <div v-for="i in 8" :key="i" class="card">
        <img src="@/assets/images/wood.png" class="thumb" />
        <p class="title">wood pallet</p>
        <p class="para">Load weight: 400 kg</p>
        <ul class="description">
          <li class="item">Length: 1200 mm, Width: 1200 mm, Height: 117 mm</li>
          <li>
            Premium wood pallets with dimensions 1200x1200x117 mm, the ideal solution for all your
            shipping and storage needs. Crafted from high-quality hardwood, these pallets offer
            exceptional durability and a robust load capacity, ensuring your goods are transported
            safely and effissciently. Perfectly designed for compatibility with a variety of
            handling equipment, our pallets streamline logistics operations, reducing time and labor
            costs. Treated to meet international standards such as ISPM 15, they are pest-resistant
            and suitable for global shipping.
          </li>
        </ul>
        <!-- <p @click="toggleDescription" class="toggle-description">Description</p> -->
        <p class="contact-us">Contact us</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const showDescription = ref(false)

const toggleDescription = () => {
  showDescription.value = !showDescription.value
}
</script>

<style scoped>
.grid-container {
  margin-right: 50px;
  margin-left: 50px;
  display: grid;
  grid-template-columns: repeat(1, 1fr);
  gap: 20px;
}

@media (min-width: 640px) {
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
    margin: 0;
  }
}

@media (min-width: 768px) {
  .grid-container {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1024px) {
  .grid-container {
    grid-template-columns: repeat(4, 1fr);
  }
}

.card {
  padding: 1rem;
  border-radius: 0.375rem;
  background-color: white;
  box-shadow:
    0 1px 3px rgba(0, 0, 0, 0.1),
    0 1px 2px rgba(0, 0, 0, 0.06);
  height: 100%;
  max-width: 600px;
  margin: 0 auto;
}

.thumb {
  max-height: 120px;
  max-width: 70%;
  display: block;
  margin: 0 auto;
}

.title {
  font-weight: bold;
  color: #6b7280; /* text-gray-500 */
  margin: 1rem 0;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.para {
  font-weight: normal;
  color: #1f2937; /* text-black-500 */
  margin: 1rem 0;
}

.description {
  font-weight: normal;
  color: #1f2937; /* text-black-500 */
  margin: 1rem 0;
}

.item {
  margin-bottom: 0.25rem;
}

.toggle-description,
.contact-us {
  background-color: #12b488;
  color: white;
  text-align: center;
  padding: 0.75rem 1rem;
  margin-bottom: 0.5rem;
  border-radius: 0.375rem;
  font-size: 0.875rem;
  cursor: pointer;
}

.contact-us {
  margin-bottom: 0;
}

@media (max-width: 600px) {
  .card {
    max-width: 100%;
    margin: 10px;
  }

  .thumb {
    max-width: 100%;
    max-height: 80px;
  }

  .text-container {
    text-align: center;
  }
}
</style>
