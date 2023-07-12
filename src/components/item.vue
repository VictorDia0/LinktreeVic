<template>
  <div>
    <a :href="item.href" target="_blank">
      <img :src="item.img" alt="Icone" />
      <span>
        {{ item.titulo }}
      </span>
    </a>
  </div>
</template>

<script>
export default {
  props: ["item"],
};
</script>

<style scoped>

div {
  display: flex;
  background-color: white;
  color: black;
  flex-direction: column;
  padding: 10px;
  text-align: center;
  width: 150px;
  margin: 20px 30px 20px 30px;
  border-radius: 20px;
}

img {
  width: 100px;
}

span {
  font-weight: 900;
}
a {
  color: black;
  text-decoration: none;
  text-transform: uppercase;
}
a:hover {
  opacity: 0.5;
}
</style>