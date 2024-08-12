<script>
	import Input from "./Input.svelte";
	
</script>


<section>
	<h1>Search Movies and Series!🍿</h1>
	<Input/>
</section>


<style>
h1 {
	font-size: 32px;
	
}
section {
	align-items: center;
	display: flex;
	flex-direction: column;
}

 @font-face {
    font-family: 'AmazonEmber';
    font-style: normal;
    font-weight: 400;
    src: local(''), local('Amazon-Ember'), url(https://fonts.cdnfonts.com/css/amazon-ember);
}

:global(body){
	font-family: 'Amazon Ember', sans-serif;
	font-family: 'Amazon Ember Cd RC', sans-serif;
	font-family: 'Amazon Ember Display', sans-serif;
	font-family: 'Amazon Ember Duospace', sans-serif;
	font-family: 'Amazon Ember Mono', sans-serif;
	font-family: 'Amazon Ember V2', sans-serif;
	color: whitesmoke;
	
}
:global(body){
	background: #121212;
}
</style>