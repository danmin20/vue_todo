<template>
    <div class="form-group">
    <input type="text" class="form-control" v-model="title" placeholder="할일을 입력해주세요." @keyup.enter="additem">
  </div>
</template>

<script lang="ts">
import {Vue, Component} from 'vue-property-decorator';
import {mapState} from "vuex";

@Component({
    computed: mapState([
        "todoList",
    ])
})
export default class ItemInput extends Vue{
    title: any = '';

    additem(){
        this.$store.commit("addItem", {
            id: (this as any).todoList.length + 1,
            title: this.title,
            status: "active",
        })
    }
}
</script>