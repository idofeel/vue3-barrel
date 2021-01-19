<template>
	<div ref="container" class="barrelContainer">
		<template v-for="(item, index) in barrelData" :key="index">
			<slot v-bind="item"></slot>
		</template>
	</div>
</template>

<script>
import userBarrel from './useBarrel'

export default {
	props: {
		data: {
			type: Array,
			default: () => []
		},
		props: {
			type: Object,
			default: () => ({
				url: 'url'
			})
		},
		baseHeight: {
			type: Number,
			default: 200
		},
		gap: {
			type: Number,
			default: 10
        },
        debounce:{
			type: Boolean || Number,
			default: false
        }
	},
	setup(props) {
		const { barrelData, container } = userBarrel(props)

		return {
			barrelData,
			container
		}
	}
}
</script>

<style scoped>
.barrelContainer{
    text-align: left;
}
.barrelContainer > * {
	display: inline-block;
	transition: all ease 0.3s;
}

.barrelContainer > * img {
	width: 100%;
}
</style>
