<template>
    <div>
        <h1>New Memory Component</h1>
        <button @click="counter++"> Increase </button>
        <p> {{ counter }}</p>
    </div>
</template>

<script>
       export default {
        data : function () {
            return {
                counter : 0
            }
        },

        destroyed() {
            console.log("destroyed")
        },

        activated(){
            console.log("activated")
        },

        deactivated(){
            console.log("deactivated")
        }
    }
</script>

