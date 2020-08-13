<template>
	<div>
		<div id="dateLine" v-for="item in data" :key="item">
				<div class="date">{{item.date}}</div>
				<div class="memo">{{item.content}}</div>
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
		height: 20px;
		margin-top: 10px;
		font-size: 15px;
		display: flex;
		justify-content: flex-start;
    .date{
			width: 150px;
			margin-left: 10px;
		}
}
</style>