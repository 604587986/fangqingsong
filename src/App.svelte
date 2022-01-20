<script>
  // 主要处理的相关绑定
  import Router from "svelte-spa-router";
  import routes from "./routes/index.js";
</script>
<!-- 这个是官方的链接跳转路由 -->
<Router {routes}/>