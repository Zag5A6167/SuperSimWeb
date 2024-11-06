<script>
    export default {
        data(){
            return {
                isDark: false
            }
        },
        methods: {
            toggleDarkMode(){
                this.isDark = !this.isDark
                document.body.classList.toggle("dark-mode")
                localStroage.setItem("dark-mode", this.isDark)
                
                

                

            }
        }
    }
</script>
<template>
    <button @click="toggleDarkMode">{{ isDark  ? 'Light mode' : 'Dark mode' }}</button>
</template>




