<template>
    <div class="flip-card">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <h1>Shut up</h1>
            </div>
            <div class="flip-card-back">
                <h1>Cierra el pico</h1>
                <div class="buttons">
                    <button class="unknow">I do not know</button>
                    <button class="know">I know</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">


</script>

<style scoped>
.flip-card {
  background-color: transparent;
  width: 250px;
  height: 300px;
  perspective: 1000px; 
}
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}
.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
}
.flip-card-front {
  background-color: #bbb;
  color: black;
  border-radius: 2rem;
  box-shadow: 5px 5px 20px 0px rgba(0,0,0,0.75);
}
.flip-card-back {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  background-color: dodgerblue;
  color: white;
  transform: rotateY(180deg);
  border-radius: 2rem;
  box-shadow: 5px 5px 20px 0px rgba(0,0,0,0.75);
}
.buttons{
  display: flex;
  flex-direction: row;
}
.unknow{
  border: 0;
  background-color: red;
  color: white;
  width: 125px;
  cursor: pointer;
  border-radius: 0 0 0 2rem;
}
.know{
  border: 0;
  background-color: green;
  color: white;
  width: 125px;
  padding: 1rem 0;
  cursor: pointer;
  border-radius: 0 0 2rem 0;
}
</style>
  