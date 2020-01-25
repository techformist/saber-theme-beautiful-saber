---
title: An Awesome Blog
layout: default
injectAllPosts: true
---

This is the greatest home page of all time.
Change this content in `pages/index.md`.

Saber + Vue form a dynamic duo. We can do amazing things on the page including a sum of two numbers.

<input v-model="a" ></input> + <input v-model="b" ></input> = <input :value="sum" style="width:60px"></input>

<script>
export default {
  data() {
    return {
        a:1,
        b:2,
     
    }
  },
  computed: {
      sum(){
          return +this.a + +this.b
      },
     
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
