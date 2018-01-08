# vue2-项目踩坑记录
安装node 安装 npm 安装webpeak 安装lic 一笔带过
下面开始介绍项目精华东西

1.a标签跳转和router-link跳转完全不同
在页面重定向中 a标签跳转多保存了一条记录，在返回的时候造成bug

例如 a->b重新向到c    a标签跳转的时候保存了b，router-link没有保存实际项目操作中也不需要

2，页面重定向，在需要保存的页面路由中记录
{
      path: '/',
      name: 'Index',
      component: Index,
      meta:{
		  keepAlive:true,
		  token:false
  	  }
    }
在router.beforeEach((to, from, next) {}里面拦截重定向具体方法参考vue-router
