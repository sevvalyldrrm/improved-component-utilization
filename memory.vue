<template>
    <div>
        <div class="memory">
            <slot name="heading"> </slot>
        </div>
        <div class="memory">
            <slot></slot>
        </div>
        <div class="memory">
            <slot name="author">
                <h3>Author</h3>
                <p>There is no content</p>
            </slot>
        </div>
    </div>

        
</template>

<script>
    export default {
    }
</script>

<style scoped>
    div.memory {
        border : 1 px solid #ddd;
        box-shadow: 1px 2px 2px 2px #666;
        padding: 20px 20px;
        margin-top: 20px;
    }
</style>