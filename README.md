# vue2-项目踩坑记录
安装node 安装 npm 安装webpeak 安装lic 一笔带过
下面开始介绍项目精华东西

1.a标签跳转和router-link跳转完全不同，在页面重定向中 a标签跳转多保存了一条记录，在返回的时候造成bug
例如 a->b重新向到c    a标签跳转的时候保存了b，router-link没有保存实际项目操作中也不需要
