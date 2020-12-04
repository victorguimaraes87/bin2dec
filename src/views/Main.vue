<template>
  <div class="main" >
    <bin2dec title="Online converter from binary to decimal" />
  </div>
</template>

<script>
// @ is an alias to /src
import bin2dec from "@/components/bin2dec.vue";

export default {
  name: "Main",
  components: {
    bin2dec
  }
};
</script>
