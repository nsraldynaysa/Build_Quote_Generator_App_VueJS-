<template>
  <div class="header">
    <h1>{{ title }}</h1>
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
  props: ['title']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  .header {
    padding: 24px 32px;
    display: flex;
    justify-content: center;

    h1 {
      font-size: 32px;
      font-weight: 600;
      color: var(--light);
      text-align: center;
      text-transform: uppercase;
      padding-bottom: 7px;
      border-bottom: 5px solid var(--primary);
    }
  }
</style>