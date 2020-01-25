---
title: First Post
layout: post
date: 2020-01-01
---

This is my first post, how exciting!

Let's do some magic to get started..

1. count clicks<br>
   <button @click="count--">-</button><input :value="count" style="width:60px;text-align:center"></input><button @click="count++">+</button>

2. reverse input<br>
   <textarea rows="4" cols="50" v-model="inputText"></textarea> >< <textarea rows="4" cols="50" :value="outputText"></textarea>

<script>
export default {
  data() {
    return {
        count:0,
        inputText:"i am groot"
    }
  },
  computed: {
      
      outputText() {
          return this.inputText && this.inputText.split('').reverse().join('')
      }
  }
}
</script>

<style>
    input {
        width:30px;
        text-align: center;
    }

    textarea{
        width:250px;
    }
</style>
