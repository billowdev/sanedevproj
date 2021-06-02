<template>
    <p class="hello">Hello {{who}}</p>
</template>
 
<script>
module.exports = {
    data: function() {
        return {
            who: 'world'
        }
    }
}
</script>
 
<style scoped>
p {
    background-color: #ffe;
}
</style>