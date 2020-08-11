<template>
  <f7-page name="todos">
    <f7-navbar large :sliding="false">
      <f7-nav-left>
        <f7-link icon-ios="f7:menu" icon-aurora="f7:menu" icon-md="material:menu" panel-open="left"></f7-link>
      </f7-nav-left>
      <f7-nav-title sliding>To-Do App</f7-nav-title>
      <f7-nav-title-large>To-Do App</f7-nav-title-large>
    </f7-navbar>

    <f7-block-title>My ToDos</f7-block-title>
    <f7-list>
        <f7-list-item link="/about/" v-for="(todo,index) in todos" v-bind:key="index" v-bind:title="todo.title" after="Edit">
        </f7-list-item>
    </f7-list>

    <f7-fab position="right-bottom" slot="fixed" color="red">
        <f7-icon ios="f7:plus" aurora="f7:plus" md="material:add">
            <f7-link href="/add/">About</f7-link>
        </f7-icon>
        
    </f7-fab>
  </f7-page>
</template>

<script>
export default {
  data() {
    return {
      todos: [{ title: "Todo 1" }, { title: "Todo 2" }, { title: "Todo 3" }],
    };
  },
};
</script>