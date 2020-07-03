<template>
    <div>
        <div>
            {{alertMessage}}
        </div>
        <div>{{parentMessage}}</div>
    </div>
</template>

<script lang="ts">
import {Component, Prop, Vue, Watch} from 'vue-property-decorator';

@Component
export default class Children extends Vue {
  @Prop() public parentMessage?: string;
  alertMessage: string = '';

  @Watch('parentMessage')
  update(value: string, oldValue: string) {
    this.alertMessage = '메시지를 업데이트 했습니다.'
  }
}
</script>

<style scoped>

</style>
