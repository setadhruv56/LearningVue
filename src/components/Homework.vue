<template>
    <div  :class="{available: available}">
        <h1 @click="changeCss" v-if="available">{{message}}</h1>
        <h1 @click="changeCss" v-else>{{text2}}</h1>
        <p>Count: {{count}}
            <button @click="resetCount">Reset Count</button>
        </p>
        <p>You pressed reset after: {{before}} clicks</p>

        <p @click="changeText">Testing 1-way Binding here: {{test}}</p>

        <input type="text" v-model="live">
        <p>{{live}}</p>
    </div>
</template> 

<script>
export default {
    name: 'Homework',
    data() {
        return {
            available: false,
            test: 'Dhruv Seta',
            message: "Now I'm green",
            text2: "I'm red",
            count: 0,
            before: 0,
            live: ''
        }
    },
    methods: {
        changeCss: function() {
            this.available = !this.available;
            this.count++;
        },

        changeText: function() {
            this.test = 'YO WTF DONT TOUCH ME'
        },

        resetCount: function() {
            console.log(this.count);
            this.before = this.count;
            this.count = 0;
        }
    }
}
</script>

<style scoped>
/* h1 {
    text-align: center;
    background-color: rgba(17, 196, 196, 0.5);
    color: rgb(15, 13, 109);
} */

h1 {
    background-color: red;
    color: white;
}

.available h1 {
    background-color: green;
}
</style>

