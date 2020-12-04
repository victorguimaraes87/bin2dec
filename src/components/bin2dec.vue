<template>
  <div  class="hellox" >
      <b-card > 
        <h1>{{ title }}</h1>
        <b-card-text>
          <input v-model="message" placeholder="Insert a binary value" maxlength = "8">
        </b-card-text>

        <b-card-text>
          <p>Decimal: "{{ reverseMessage() }}"</p>
          <p>{{ binary }}</p>
        </b-card-text>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "bin2dec",
  props: {
    message: String,
    error: String,
    title: String,
    binary: String
  },
  methods: {
      reverseMessage: function () {

        for (var prop in this.message) {
          console.log("obj." + prop + " = " + this.message[prop]);
          if (this.message[prop] !== "0" && this.message[prop] !== "1") {
            return "is not a binary"; 
          }
        }
        
        if (this.message) {
           return parseInt(this.message, 2);
        }
         return 0;
      }
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.hellox {
  margin-top: 10%;
}

</style>
