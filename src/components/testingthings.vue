<template>
  <div>Remember, you have got {{ shit }} seconds to run!</div>
  <button :disabled="isDisabled">Spit</button>
  <div @click="switchDisabled">
    {{ disabledText }}
  </div>
  <div @click="increment" :class="[shit >= 30 ? classes.overThirty: shit >= 20 ? classes.overTwenty : shit >= 10 ? classes.overTen : classes.underTen]" >
     Increase the value 
  </div>
</template>

<script>

export default {
    name: 'ShitPants',
    data() {
        return {
            shit: 0,
            isDisabled: false,
            classes: {
                overThirty: 'overthirty',
                overTwenty: 'overtwenty',
                overTen: 'overten',
                underTen: 'underten'
            }
        }
    },
    methods: {
        switchDisabled() {
            this.isDisabled = !this.isDisabled
        },
        increment() {
            this.shit += 10
        }
    },
    computed: {
        disabledText() {
            return this.isDisabled ? 'Unblock the button' : 'Block the button'
        }
    }
}

</script>


<style>

.coco{
    color: red;
}

.overthirty{
    background: blue;
    color: darkgreen;
}
.overtwenty{
    background: darkgreen;
    color: blue;
}
.overten{
    background: black;
    color: darkred;
}
.underten{
    background: darkred;
    color: black;
}

</style>