<script>

export default {
  mounted() {
    const changeColorBtn = document.getElementById('changeColorBtn');
    const h1 = document.querySelector('.jumbotron-content h1');

    const colors = ['#FF5733', '#33FF57', '#5733FF', '#FFFF33', '#33FFFF', '#FF33FF', '#333333', '#FFFFFF'];
    let currentIndex = 0;

    changeColorBtn.addEventListener('click', () => {
      h1.style.color = colors[currentIndex];
      currentIndex = (currentIndex + 1) % colors.length;
    });
  },
  methods: {
    changeColor() {
      this.$emit('change-color');
    }
  }
};

</script>

<template>

    <div class="jumbotron">
        <div class="jumbotron-content">
            <div class="empty">
                <h1>QUESTO E' IL MIO PRIMO JUMBOTRON INTERATTIVO (se così possa chiamarsi....)</h1>
                <button id="changeColorBtn" class="btn">Cliccami!!</button>
            </div>
        </div>
    </div>

</template>

<style>

.jumbotron {
  background-image: url('https://www.cantinedidolianova.it/wp-content/uploads/2020/11/shutterstock_571564606-1.jpg');
  background-size: cover;
  height: calc(100vh - 48px);
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  text-align: center;
}

.jumbotron-content {
  max-width: 600px;
  padding: 20px;
  margin-bottom: 300px;
}

.jumbotron h1 {
  font-size: 36px;
  margin-bottom: 20px;
}

.jumbotron p {
  font-size: 18px;
  margin-bottom: 20px;
}

.btn {
  padding: 10px 20px;
  background-color: green;
  color: #fff;
  text-decoration: none;
  border-radius: 6px;
  border-color: greenyellow;
  transition: background-color 0.4s;
  cursor: pointer;
}

.btn:hover {
  background-color: seagreen;
}

.empty {
    background-color: forestgreen;
    border-radius: 24px;
    padding: 20px;
    opacity: 0.6;
}

</style>