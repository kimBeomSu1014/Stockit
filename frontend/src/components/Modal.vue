<template>
    <div class="modal-overlay" @click.self="$emit('close')">
            <slot></slot>
    </div>
</template>

<script>
export {};
</script>

<style scoped>
.modal-overlay {
    position: fixed;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    padding: 20px;
}
</style>
