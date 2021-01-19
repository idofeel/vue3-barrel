<template>

	<Vue3Barrel :data="list" :baseHeight="200" :gap="20" :debounce="200">
		<template #default="item">
			<div
				:style="
					`width:${item.width}px;height:${
						item.height
					}px;margin:${item.margin / 2}px`
				"
			>
				<img :src="item.src" alt="" />
				{{ item.title }}
			</div>
		</template>
	</Vue3Barrel>
</template>

<script>
import { ref } from 'vue'
import Vue3Barrel from '@/components/vue3-barrel'
export default {
	name: 'App',
	components: {
		Vue3Barrel
	},
	setup() {
		const list = ref([
			{
				url:
					'https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=3363295869,2467511306&fm=26&gp=0.jpg',
				title: '标题标题'
			},
			{
				url:
					'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa2.att.hudong.com%2F27%2F81%2F01200000194677136358818023076.jpg&refer=http%3A%2F%2Fa2.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1613554112&t=4fecf12e0fbca98667b9565f6489962d',
				title: '标题标题'
			},
			{
				url:
					'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=1089874897,1268118658&fm=26&gp=0.jpg',
				title: '标题标题'
			},
			{
				url:
					'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=2853553659,1775735885&fm=26&gp=0.jpg',
				title: '标题标题'
			},
			{
				url:
					'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fs9.sinaimg.cn%2Fbmiddle%2F5ceba31bg5d6503750788&refer=http%3A%2F%2Fs9.sinaimg.cn&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1613554112&t=afcba622f562489529f07a7cbc68879c',
				title: '标题标题'
			},
			{
				url:
					'https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fa3.att.hudong.com%2F02%2F38%2F01300000237560123245382609951.jpg&refer=http%3A%2F%2Fa3.att.hudong.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1613554112&t=5a671def53664b0718a65f8a526dcccb',
				title: '标题标题'
			},
			{
				url:
					'https://ss3.baidu.com/-fo3dSag_xI4khGko9WTAnF6hhy/zhidao/pic/item/5366d0160924ab18c1375d8835fae6cd7b890b6f.jpg',
				title: '标题标题'
			}
		])
		return {
			list
		}
	}
}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
