<template>
	<div>
		<div id="dateLine" v-for="item in data" :key="item">
				<div class="date">{{item.date}}</div>
				<div class="content">{{item.content}}</div>
		</div>
	</div>
</template>

<script>
export default {
    props:{
        data:Array
    }
}
</script>

<style lang='scss'>
#dateLine{
    position: relative;
		height: 20px;
		margin-top: 6px;
		font-size: 15px;
    .date{
        position: absolute;
    }
    .content{
        position: absolute;
        left: 150px;
    }
}
</style>