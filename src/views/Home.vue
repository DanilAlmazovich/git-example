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
    this.people.push({
      name: 'John',
      type: 'mentor',
      color: 'red'
    })
    //здесь будете пушить свои данные
    this.people.push({
      name: 'Nikita',
      type: 'student',
      color: 'orange'
    }),
    this.people.push({
      name: 'AbuBandit',
      type: 'student',
      color: 'yellow'
    })
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
  .list .bg-red {
    background: #fd0d0d;
  }
  .list .bg-orange {
    background: orange;
  }
  .list .bg-yellow {
    background: rgb(242, 255, 0);
  }
</style>
