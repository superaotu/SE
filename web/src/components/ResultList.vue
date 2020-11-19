<template>
	<div class="column">
		
		<div class="column item-box"  v-for="(item,index) in res_list" :key="index">
			<a class="cut" :href="item.link_url">{{item.title}}</a>
			<p class="cut">{{item.desc}}</p>
			<span>{{item.from_web}}</span>
		</div>
		
		
	</div>
</template>

<script>
	export default {
	  name: 'ResultList',
	  props: {
	    msg: String
	  },
	  setup(){
		
		let res_list = [
			{
				title:"关闭ESlint 语法检测配置方法 - simple-love - 博客园",
				desc:"2019年10月22日 关闭eslint 这里只说vue-cli脚手架的关闭方法,其实很简单,就是把 build/webpack.base.conf.js 配置文件中的eslint rules注释掉即可。",
				link_url:"www.baidu.com",
				from_web:"www.baidu.com"
			},{
				title:"详解关闭令人抓狂的ESlint 语法检测配置方法_javascript技...",
				desc:"2019年10月28日 这篇文章主要介绍了详解关闭令人抓狂的ESlint 语法检测配置方法,文中通过示例代码介绍的非常详细,对大家的学习或者工作具有一定的参考学习价值,需要的...",
				link_url:"www.baidu.com",
				from_web:"www.baidu.com"
			}
		]
		
		
		
	    return { res_list }
	  }
	}
	
	
</script>

<style scoped="scoped">
	a{
		text-decoration: none;
		color: black;
		font-weight: bold;
	}
	
	a:visited{
		color: #005CC5;
	}
	p{
		margin: 0.25rem 0;
	}
	.item-box{
		margin: 1.25rem;
	}
	.cut{
	    display: inline-block;        /*让span 标签变成行内标签但具有宽高属性*/
	    white-space: nowrap;         /*文本不进行换行*/
	    overflow: hidden;           /*隐藏溢出文本*/
	    text-overflow: ellipsis;   /*多出文本使用 ....代替*/
	    width: 60%; 
	}
</style>
