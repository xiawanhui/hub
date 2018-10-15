<template>
    <div id="teachers">
        <h2>{{title}}</h2>
        <ol>
            <li v-for="teacher in teachers" :key='teacher.id'>
                {{teacher.name}}:{{teacher.age}}
            </li>
        </ol>
        <router-link to="students">点击跳转到students</router-link>
    </div>
</template>

<script>
    export default {
        name: 'teachers',
        data: function() {
            return {
                teachers: [
                    {name: 'wang', age: '40'},
                    {name: 'xia', age: '41'},
                    {name: 'wu', age: '42'}
                ],
                title: 'this is teacher'
            };
        }
    };
</script>

<style scoped>
#teachers{
    background: blue
}
</style>