<template>
  
<div class="unique-card">
  <div class="background-overlay"></div>
  <div class="card-content">
    <div class="card-title">GET A TICKET </div>
    <div class="card-description"><h1>
        <bold>{{price}}$</bold>
    </h1> </div>
  </div>
</div>


</template>

<script>
export default {
  props: {
    price: {
      type: Number, 
      required: true,
    },
  },
};
</script>

<style scoped>
.unique-card {
  position: relative;
  width: 100%;
  height: 200px;
  overflow: hidden;
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s, box-shadow 0.3s;
}

.unique-card:hover {
  transform: scale(1.1);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
}

.card-content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
  color: #888;
  z-index: 2;
  transition: color 0.3s;
}

.unique-card:hover .card-content {
  color: #ec008c;
}

.background-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(52, 73, 94, 0.7);
  border-radius: 15px;
  opacity: 0;
  transition: opacity 0.3s;
}

.unique-card:hover .background-overlay {
  opacity: 1;
}

.card-title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 10px;
}

.card-description {
  font-size: 16px;
}

</style>