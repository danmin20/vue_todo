<template>
    <div class="form-group">
    <input type="text" class="form-control" placeholder="할일을 입력해주세요." @keyup.enter="additem">
  </div>
</template>

<script lang="ts">
import {Vue, Component} from 'vue-property-decorator';

@Component
export default class ItemInput extends Vue{
    additem(){
        return 0;
    }
}
</script>