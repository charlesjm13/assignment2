<!--GUIDE: here is a reusable component. 
This component could theoretically be added to and initialized in any vue app as long as it was passed the three props it requires -->
<template lang="html">
  <div class="comment">
    <h4>by <a href="">{{ user.username }}</a> on {{ created }}</h4>
    <p v-html="content"></p>
  </div>
</template>

<script>
export default {
    name: 'comment',
    props: [
        'user',
        'created',
        'content'
    ],
    data() {
        return {}
    }
}
</script>

<style scoped lang="css">
.comment {
    background: #f2f2f2;
    padding: 20px 10px;
    margin-bottom: 20px;
}

h4 {
    margin: 5px 0;
}

p {
    margin: 5px 0;
}
</style>
