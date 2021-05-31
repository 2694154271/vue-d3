ue+d3 支持 节点点击之后出现数据， 单个节点可以用图片显示， 单个节点可以拖动， 整个页面可以缩放


项目

npm install 
npm run serve
```vue
<template>
  <div id="app">
    <network :nodeList="nodes" :linkList="links"></network>
  </div>
</template>

<script>

export default {
  name: "app",
  components: {
    Network
  },
  data() {
    return {
      nodes: [
      	{"id": "Myriel", "group": 1},
      	{"id": "Napoleon", "group": 1},
        {"id": "Labarre", "group": 2},
        {"id": "Valjean", "group": 2}
      ],
      links: [
        {"source": "Napoleon", "target": "Myriel", "value": 1},
        {"source": "Valjean", "target": "Labarre", "value": 1},
        {"source": "Napoleon", "target": "Valjean", "value": 2},
      ]
    };
  },
};
</script>