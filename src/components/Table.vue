<template>
    <div class="container">
        <div v-for="elementData in elementDataList" :key="elementData.atomicNumber">
            <Element
                :name="elementData.name"
                :atomicNumber="elementData.atomicNumber"
                :color="(elementData.cpkHexColor).toString()"
            />
        </div>
    </div>
</template>

<script>
import Element from "./Element.vue";
export default {
    name: "Table",
    mounted() {
        this.getElementData();
    },
    data() {
        return {
            elementDataList: [],
        };
    },
    methods: {
        getElementData() {
            fetch("data/data.json")
                .then(response => response.json())
                .then(data => (this.elementDataList = data));
        }
    },
    components: { Element }
}
</script>

<style>
.container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
}
</style>