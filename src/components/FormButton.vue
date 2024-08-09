

<template>
    <button :type="button" class="btn btn-primary">>{{ text }}</button>
</template>
<script>

export default {
    props: {
        text: {
            type: String,
            required: true
        },
        type: {
            type: String,
            required: true
        }
    }
}
</script>
<style scoped>
</style>