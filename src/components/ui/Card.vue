<template>
    <div class="card">
        <slot></slot>
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.card {
    width: 100%;
    margin-top: 10px;
    border-radius: 4px;
    border-top:3px solid purple;
    padding: 10px;
    box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px, rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
}
</style>