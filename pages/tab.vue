<template>
	<div style="padding:100px;">
		<div class="button">
			<span v-for="(item, index) in ['新闻', '八卦', '体育']"
            :key="index"
            @click="handleClick(index)"
            :class="{ active: current === index }">
                {{item}}
            </span>
		</div>

		<div v-if="current === 0">
			<ul>
				<li>美国装逼失败</li>
				<li>伊，俄，中，三国军事演练</li>
				<li>伊拉克吐槽美国</li>
			</ul>
		</div>
		<div v-if="current === 1">
			<ul>
				<li>古校长官宣恋情</li>
				<li>杨丞琳穿蓝色深V亮片裙晒美照 眼神魅惑撩人</li>
				<li>张利华再被曝出轨 魏骏杰个人简介已改成 离婚</li>
			</ul>
		</div>
		<div v-if="current === 2">
			<ul>
				<li>埃里克森告别热刺？国米冬窗补强要打包他和吉鲁</li>
				<li>官方：门兴年轻后卫拜尔租借加盟汉堡</li>
				<li>法国足球：努贝尔加盟拜仁后，尤文考虑引进诺伊尔</li>
			</ul>
		</div>
	</div>
</template>

<script>
export default {
    data(){
        return {
            // 当前高亮的状态索引
            current: 0,
        }
    },

    methods: {
        handleClick(index){
            this.current = index;
        }
    }
};
</script>

<style scoped>
.button span{
    cursor: pointer;
    padding-right: 20px;
}

.active{
    color: red;
}
</style>