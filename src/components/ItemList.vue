<template>
    <draggable :list="items" >
        <el-card v-for="(item, i) in items" :key="i">
            {{ item.name }} costs you {{ item.price }} {{ item.interval }}
        </el-card>
    </draggable>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import draggable from 'vuedraggable';

@Component({
    components: {
        draggable
    }
})
export default class HelloWorld extends Vue {
  @Prop() private items!: [{name: String, price: Number, interval: String}];

}
</script>

<style scoped>
    .el-card {
        margin-bottom: 20px;
    }
</style>