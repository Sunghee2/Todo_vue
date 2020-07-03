<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <h1>약관</h1>
    <p>이곳에는 동의를 필요하는 어떠한 약관 내용이 들어갑니다.</p>
    <my-check-box v-model="checked" @change="change"></my-check-box>
    {{text}}
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import {Component, Vue, Provide} from 'vue-property-decorator';
import myCheckBox from '@/components/my-checkbox.vue';

@Component({
  components: {
    myCheckBox,
  },
})

export default class Home extends Vue {
  checked: boolean = false;
  text: string = '동의하지 않습니다.';

  change(checked: boolean) {
    this.checked = checked;
    this.text = checked? '동의합니다.' : '동의하지 않습니다.';
  }
}
</script>
