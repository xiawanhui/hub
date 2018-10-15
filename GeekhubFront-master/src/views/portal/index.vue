<template>
    <div id="portal">
        <h2> {{title}}</h2>
        <nav>
            <logo />
        </nav>
        <div>
            <h1>portal</h1>
        </div>
        <students :students='students' v-on:titlechanged='uptitle($event)'></students>
        <teachers></teachers>
    </div>
</template>

<script>
import logo from '../common/logo.vue';
import students from '../common/students.vue';
import teachers from '../common/teachers.vue';

export default {
    name: '',
    data: function() {
        return {
            students: [
                {
                    id: 1,
                    name: 'xiaoha',
                    age: 18
                },
                {
                    id: 2,
                    name: 'huahua',
                    age: 18
                },
                {
                    id: 3,
                    name: 'xiaoxiao',
                    age: 18
                }
            ],
            title: '这是父组件'
        };
    },
    components: {
        logo,
        students,
        teachers
    },
    methods: {
        uptitle: function(title) {
            this.title = title;
        }
    }
};
</script>

<style lang="scss" scoped>
a{
    color: red
}
</style>