<script>
export default {
    props: {
        cardImage: String,
        cardTitle: String,
        cardPrice: String
    }
};

</script>

<template>
<div>
    <img 
    :src="cardImage"
    :alt="cardTitle">
    <h4>{{cardTitle}}</h4>
    <h6>{{cardPrice}}</h6>
</div>
</template>

<style scoped lang="scss">

</style>