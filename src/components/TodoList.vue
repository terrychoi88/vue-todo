<template>
    <section>
        <transition-group name="list" tag="ul">
            <li :key="index" :value="todoItem" v-for="(todoItem,index) in propsdata" class="shadow">
                <i class="checkBtn fas fa-check" aria-hidden="true"></i>
                {{todoItem}}
                <span class="removeBtn" type="button" @click="removeTodo(todoItem, index)">
                    <i class="far fa-trash-alt" aria-hidden="true"></i>
                </span>
            </li>
        </transition-group>
    </section>
</template>

<script>
export default {
    props: ['propsdata'],
    methods: {
        modifyTodo(t, i) {
            this.$emit('removeTodo', t, i);
        },
        removeTodo(t, i) {
            this.$emit('removeTodo', t, i);
        }
    }
}
</script>

<style scoped>
    ul {
        list-style-type: none;
        padding-left: 0px;
        margin-top: 0;
        text-align: left;
    }
    li {
        display: flex;
        min-height: 50px;
        height: 50px;
        line-height: 50px;
        margin: 0.5rem 0;
        padding: 0 0.9rem;
        background: white;
        border-radius: 5px;
    }
    .checkBtn {
        line-height: 47px;
        color: green;
        margin-right: 6px;
    }
    .removeBtn {
        margin-left: auto;
        color: #de4343;
    }
    .list-enter-active, .list-leave-active {
        transition: all 1s;
    }
    .list-enter, .list-leave {
        opacity: 0;
        transform: translateY(30px);
    }
</style>