<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    },
  },
};
</script>

<template>
  <main>
    <div>
      <h1>Counter</h1>
      <span id="value">{{ count }}</span>
      <div>
        <button @click="decrement" id="decrement">-</button>
        <button @click="increment" id="increment">+</button>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  text-align: center;
  background-color: #333333;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 0 1rem 0 rgba(0, 0, 0, 0.2);
}

h1 {
  color: #ffffff;
}

#value {
  font-size: 50px;
  color: #ffffff;
}

button {
  font-size: 16px;
  margin: 0 5px;
  background-color: #555555;
  color: #ffffff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 5px;
}

button:hover {
  background-color: #777777;
}

button:active {
  animation: pulse 0.5s linear;
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
</style>
