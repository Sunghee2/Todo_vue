<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Message></Message>
    <children :parentMessage="message"></children>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import {Component, Vue} from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue';
import Message from '@/components/message';
import children from '@/components/children';

@Component({
  components: {
    Message,
    children,
  },
})

export default class Home extends Vue {
  public message: string = 'send message';
}
</script>
