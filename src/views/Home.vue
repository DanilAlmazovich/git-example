<template>
  <div class="container">
      <div class="list">
        <div class="item" v-for="person in people" :class="`bg-${person.color}`">
          <span class="name">{{ person.name }}</span>
          <span>-</span>
          <span class="type">{{ person.type }}</span>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      people: []
    }
  },
  mounted() {
    this.people.push({
      name: 'Danil',
      type: 'mentor',
      color: 'purple'
    })
    //здесь будете пушить свои данные
  }
}
</script>

<style>
  .list {
    display: flex;
    flex-wrap: wrap;
  }
  .list .item {
    width: 50%;
    display: flex;
    color: white;
    font-size: 22px;
    padding: 30px 10px;
    justify-content: center;
    font-weight: 500;
  }
  .list .item .name {
    margin-right: 10px;
  }
  .list .item .type {
    margin-left: 10px;
  }
  .list .bg-purple {
    background: #810281;
  }
</style>