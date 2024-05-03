<script>
export default {
    props: {
        cardImage: String,
        cardTitle: String
    }
};

</script>

<template>
<div>
    <img 
    :src="cardImage"
    :alt="cardTitle">
    <h4>{{cardTitle}}</h4>
</div>
</template>

<style scoped lang="scss">

</style>