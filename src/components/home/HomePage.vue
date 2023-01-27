<template>
  <div class="mainContainer">
    <div class="searchContainer">
      <div class="searchBar">
        <input
          type="search"
          placeholder="search"
          v-model="search"
          class="searchBox"
        />
        <div class="serchIcon">
          <img src="../../assets/search.png" alt="search" class="icon" />
        </div>
      </div>
      <div class="searchResult" v-if="result.length != 0">
        <ul class="result">
          <li>list</li>
          <hr />
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "HomePage",
  components: {},
  data() {
    return {
      search: "",
      result: [],
    };
  },
  methods: {},
};
</script>
<style scoped>
.mainContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100vh;
  border: 1px solid;
}
.searchContainer {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  width: 41%;
  height: 45%;
  border-radius: 8px;
  border: none;
  box-shadow: 0px 5px 24px 4px grey;
  overflow: hidden;
}
.searchBar {
  border: 1px solid;
  width: 66%;
  height: 10%;
  border-radius: 5px;
  margin-top: 3%;
  display: flex;
}
.searchBox {
  width: 86%;
  text-align: center;
  font-size: 16px;
  font-family: helvetica;
  color: black;
}
.serchIcon {
  border: 1px solid;
  width: 13%;
}
.icon {
  width: 100%;
  height: 100%;
}
.icon:active {
  background: rgb(42, 42, 243);
}
.searchResult {
  border: none;
  position: absolute;
  z-index: 2;
  background: #f5f5f5bd;
  width: 33%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0px 0px 10px 0px grey;
  margin-top: 6%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.result {
  list-style: none;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  padding: 0px;
  width: 75%;
  height: auto;
  font-size: 15px;
  font-family: helvetica;
}
hr {
  width: 100%;
  border: 0.2px solid;
}
</style>
