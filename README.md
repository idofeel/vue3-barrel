# vue3-barrel
### vue3.0x 
## 使用方式

```
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

import Vue3Barrel from '@/components/vue3-barrel'

export default {
	components: { Vue3Barrel },
}
</script>
```