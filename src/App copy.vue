<template>
  <div id="app">
    <!--  工具栏  -->
    <nav class="navbar navbar-default navbar-fixed-top">
      <div class="container">
        <div class="navbar-header">
          <a class="navbar-brand">vue-memo</a>
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target=".navbar-collapse" aria-expanded="false">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
        </div>
        <div class="collapse navbar-collapse navbar-right">
          <ul class="nav navbar-nav">

            <!--  新建  -->
            <li class="add dropdown">
              <a class="create-new dropdown-toggle" data-toggle="dropdown">新建</a>
              <ul class="dropdown-menu">
                <li @click="createMarkdown">
                  <a>Markdown</a>
                </li>
                <li @click="createDoodle">
                  <a>涂鸦</a>
                </li>
              </ul>
            </li>
            <!--  -->

            <!--  类别过滤器  -->
            <li class="categories dropdown">
              <a class="current-category dropdown-toggle" data-toggle="dropdown">
                {{ categories[currentCategoryId] }}
                <span class="count badge">{{ memosFiltered.length }}</span>
              </a>
              <ul class="dropdown-menu">
                <li class="total" @click="filterBy(0, queryString)">
                  <a>
                    全部
                    <span class="count badge">{{ memos.length }}</span>
                  </a>
                </li>
                <li class="divider"></li>
                <li @click="filterBy(1, queryString)">
                  <a>
                    工作
                    <span class="count badge">{{ memosInWorkCate.length }}</span>
                  </a>
                </li>
                <li @click="filterBy(2, queryString)">
                  <a>
                    生活
                    <span class="count badge">{{ memosInLivingCate.length }}</span>
                  </a>
                </li>
                <li @click="filterBy(3, queryString)">
                  <a>
                    学习
                    <span class="count badge">{{ memosInStudyCate.length }}</span>
                  </a>
                </li>
              </ul>
            </li>
            <!--  -->

            <!--  排序器  -->
            <li class="sort-by dropdown">
              <a class="dropdown-toggle" data-toggle="dropdown">
                {{ currentSortBy }}
              </a>
              <ul class="dropdown-menu">
                <li @click="sortByTimeOrTitle('title')">
                  <a>按标题排序</a>
                </li>
                <li @click="sortByTimeOrTitle('timeStamp')">
                  <a>按创建时间排序</a>
                </li>
              </ul>
            </li>
            <!--  -->

            <!--  字符串过滤器  -->
            <li>
              <input
                type="text"
                class="search-box form-control"
                placeholder="过滤标题、内容、时间戳"
                v-model="queryString"
                @keyup="filterBy(currentCategoryId, queryString)">
            </li>
            <!--  -->

          </ul>
        </div>
      </div>
    </nav>
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
