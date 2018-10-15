<template>
    <div id="students">
        <h2>{{title}}</h2>
        <ul>
            <li v-for="student in students" :key="student.id">{{student.name}}的年龄{{student.age}}</li>
        </ul>
        <button v-on:click='changetitle'>点击向父组件传title</button><br>
        <router-link to='/teachers'>点击跳转到teachers</router-link>
    </div>
</template>

<script>
    export default {
        name: 'students',
        props: {
            students: {
                type: Array
            }
        },
        data: function() {
            return {
                title: 'this is students'
            };
        },
        methods: {
            changetitle: function() {
                this.$emit('titlechanged', '改变后的title');
            }
        }
    };
</script>

<style scoped>
a{
    color: red
}
#students{
    background: yellow
}
</style>