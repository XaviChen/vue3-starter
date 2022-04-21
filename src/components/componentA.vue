<script setup lang="ts">

import { ref } from "vue"

const data = "Charlie";
const text = ref<string>("棒!!!");
const view = ref<number>(1);
const handlerChang = (index: number) => {
    view.value = index
}

</script>

<template>
    <button @Click="handlerChang(1)">View1</button>
    <button @Click="handlerChang(2)">View2</button>
    <button @Click="handlerChang(0)">No</button>
    <div v-if="view === 1">
        <p>Hello {{ data }}</p>
    </div>

    <div v-else-if="view === 2">
        <p>{{ text }}</p>
        <input type="text" v-model="text" />
    </div>

    <div v-else>
        <p>No Page</p>
    </div>
</template>


