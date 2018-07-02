<template>
	
	<div>
		{{msg}}

		<br>

		<button @click="run()">触发事件</button>
		<br>
		<br>

		<ul>
			<li v-for="(item,key) in list":key="key">
				{{item}}
			</li>
		</ul>

		<img src="../../../static/images/home2.png">
	</div>
</template>

<script>
	//创建必须暴露
	export default{
		data(){
			return{
				msg:'我是一个新闻组件',
				list:[]
			}
		},
		methods:{
			run(){
				console.log('执行方法')
			}
		},
		// 生命周期函数
		created(){
			for(var i=0;i<10;i++){
				this.list.push('我是第'+i);
			}
		}
	}
</script>