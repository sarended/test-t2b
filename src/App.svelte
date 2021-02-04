<script>
	const categories = [
		{'name' :'روغن موتور', 'class' : 'fa-oil-can'},
		{'name' :'لاستیک', 'class' : 'fa-galactic-republic'},
		{'name' :'باتری', 'class' : 'fa-car-battery'},
		{'name' :'کارواش', 'class' : 'fa-car-crash'},
		{'name' :'لنت', 'class' : 'fa-cuttlefish'},
		{'name' :'شمع', 'class' : 'fa-menorah'},
	];
	
	const products = [
		{'name' :'روغن موتور SG مدل (50-20W) تکتاز حجم 4 لیتر بهران', 'img' : 'https://api.t2bon.com/media/statics/images/%D8%AA%DA%A9%D8%AA%D8%A7%D8%B2.jpg', 'price' : '110,000'},
		{'name' :'روغن موتور SJ مدل (50-20W) پیشتاز حجم 4 لیتر بهران', 'img' : 'https://api.t2bon.com/media/statics/images/%D8%A8%D9%87%D8%B1%D8%A7%D9%86-%D9%BE%DB%8C%D8%B4%D8%AA%D8%A7%D8%B2_75Zgw89_rznWhRN.jpg', 'price' : '120,000'},
		{'name' :'روغن موتور SL مدل سوپرپيشتاز (20W-50) حجم4لیتر بهران', 'img' : 'https://api.t2bon.com/media/statics/images/%D8%B3%D9%88%D9%BE%D8%B1%D9%BE%DB%8C%D8%B4%D8%AA%D8%A7%D8%B2.jpg', 'price' : '135,000'},
		{'name' :'روغن موتور SL مدل سوپرپيشتاز (10W-40) حجم4لیتر بهران', 'img' : 'https://api.t2bon.com/media/statics/images/%D8%B1%D9%88%D8%BA%D9%86-%D9%85%D9%88%D8%AA%D9%88%D8%B1-SL-%D9%85%D8%AF%D9%84-%D8%B3%D9%88%D9%BE%D8%B1%D9%BE%D9%8A%D8%B4%D8%AA%D8%A7%D8%B2-10W-40-%D8%AD%D8%AC%D9%854%D9%84%DB%8C%D8%AA%D8%B1-%D8%A8%D9%87%D8%B1%D8%A7%D9%86_0W3wbOz.jpg', 'price' : '185,000'},
		{'name' :'سبد روغن موتور TX مدل(50-20W)+ فیلتر هوا ویژه پراید معمولی', 'img' : 'https://api.t2bon.com/media/statics/images/TX_20W-50-_%D8%B6%D8%AF%DB%8C%D8%AE.jpg', 'price' : '159,000'},
	];
		
</script>

<main>
	<header>
		<div class="header-child">
			<div class="header-item">
				<i class="fas fa-bars"></i>
			</div>
			<div class="header-item">
				<img class="logo" src="./logo.png" alt="">
			</div>
			<div class="header-item">
				<i class="fas fa-wallet"></i>
			</div>
		</div>
		<!-- <div>
			<input class="search" type="text" placeholder="دنبال چی می‌گردی؟">
			<i class="fas fa-search search-icon"></i>
		</div> -->
		<nav>
			<!-- <p class="imp-text">دسته بندی محصولات</p> -->
			<div class='navbar'>
				<div class="box">
					{#each categories as cat,i }
						<span class="navbar-btn">
							<i class={i===1 || i===4?'category fab '+cat.class :'category fas '+cat.class}></i>
							<p class="cat-text">{cat.name}</p>
						</span>
					{/each}
				</div>
			</div>
		</nav>
	</header>
	<section class="body">
		<section>
			<h1 class="title">پرفروش ترین محصولات</h1>
			<div class='navbar'>
				<div class="box">
					{#each products as pro,i }
						<span class="navbar-btn product-container">
							<img class="pro-img" src={pro.img} alt={pro.name}>
							<div class="hover">
								<p class="cat-text pro-text">{pro.name}</p>
								<p class="pro-text pro-price">{pro.price}تومان</p>
							</div>
						</span>
					{/each}
				</div>
			</div>
		</section>
		<div>
			<img class="banner" src="https://api.t2bon.com/media/slider_images/banner_mobile_tire.jpg" alt="t2b">
		</div>
		<section>
			<h1 class="title">روغن موتور</h1>
			<div class='navbar'>
				<div class="box">
					{#each products as pro,i }
						<span class="navbar-btn product-container">
							<img class="pro-img" src={pro.img} alt={pro.name}>
							<div class="hover">
								<p class="cat-text pro-text">{pro.name}</p>
								<p class="pro-text pro-price">{pro.price}تومان</p>
							</div>
						</span>
					{/each}
				</div>
			</div>
		</section>
	</section>
	<div class="fdesign" />
	<footer class="footer">
		<span class="selected">
			<i class="fas fa-home"></i>
			<p>خانه</p>
		</span>
		<!-- <i class="fas fa-border-all"></i> -->
		<i class="fas fa-car-alt"></i>
		<i class="fas fa-warehouse"></i>
		<i class="fas fa-shopping-cart"></i>
	</footer>
</main>

<style>
	main {
		width: 100%;
		height: 100vh;
		background-color: #fefefe;
		font-family: yekan, sans-serif;
		overflow: hidden;
		display: flex;
    	flex-direction: column;
	}

	header {
		padding: 5px 20px 15px;
		/* height: 500px; */
		background-color: #202d53;
		color: #fefefe;
		/* border-radius: 0 0 30px 30px; */
	}
	.header-child {
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.header-item {
		display: flex;
		align-items: center;
		justify-content: center;
		height: 50px;
	}

	.logo {
		width: 100px;
	}

	.search {
		margin-top: 10px;
		width: 100%;
		height: 50px;
		border-radius: 12px;
		font-family: yekan;
		font-size: 15px;
		font-weight: 400;
		padding: 0 10px;
		box-sizing: border-box;
		color: #bbb;
		border: none;
	}

	.search-icon {
		display: inline;
		position: absolute;
		top: 81px;
		left: 35px;
		color : #bbb;
	}

	.imp-text {
		margin: 20px 0 10px;
	}

	.navbar {
		width: calc(100% + 20px);
		display: flex;
		flex: 1;
		overflow: auto;
		margin: 15px 0 0;
	}

	.box {
		display: flex;
    	min-height: min-content;
	}

	.navbar-btn {
		width: 80px;
		display: flex;
		justify-content: center;
		align-items: center;
		text-align: center;
		flex-direction: column;
	}

	.category {
		background-color: #364264;
		color: #f3f3f3;
		width: 50px;
		height: 50px;
		border-radius: 8px;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.cat-text {
		font-size: 14px;
		font-weight: normal;
	}

	.body {
		flex-grow: 1;
		/* border-radius: 0 0 30px 30px; */
		background-color: white;
		z-index: 2;
		padding: 10px 25px 25px;
		max-height: 590px;
		overflow-y: scroll;
		box-sizing: border-box;
	}

	.title {
		font-size: 16px;
		font-weight: normal;
		margin-bottom: 10px;
	}

	.product-container {
		font-size: 12px;
		width: 100px;
		margin-left: 20px;
		border-radius: 25px;
		height: 170px;
		overflow: hidden;
		border: 1px solid #313131;
		padding: 0 5px 10px;
	}

	.pro-img {
		width: 100px;
	}

	.hover {
		background-color: white;
		width: 100px;
		font-size: 12px;
		color: #313131;
	}

	.pro-text {
		font-size: 12px;
		color: #313131;
	}

	.pro-price {
		color: deeppink;
    	font-size: 14px;
	}

	.banner {
		width: 100%;
		border-radius: 25px;
		margin-top: 25px;
	}

	.fdesign {
		background-color: #0a0d14;
		height: 70px;
		display: none;
	}

	.footer {
		background-color: #0a0d14;
		width: 100%;
		height: 100px;
		align-self: flex-end;
		color: #ccc;
		position: absolute;
		bottom: 0;
		left: 0;
		z-index: 1;
		padding: 30px 30px 2px;
		display: flex;
		flex-direction: row;
		box-sizing: border-box;
		justify-content: space-between;
		align-items: center;
	}

	.selected {
		/* color: white; */
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 65px;
		font-weight: bold;
		border-radius: 50px;
		padding: 2px 15px;
		background-color: #cdced0;
		color: #0a0d14;
	}

</style>

	<!-- 
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	// font size
	$font-text: 14px;
	$font-title: 18px;
	$font-stitle: 16px;
	$font-text-low: 12px;
	$border-radius: 100px;
	$border-radius-low: 6px;
	
	// main colors
	$primary: #f0008b;
	$secondary: #00acec;
	
	// bg
	$main-bg: #ddd;
	$bg-primary: #2b328b;
	$bg-secondary: #7f3f98;
	$bg-rare: #7351c9;
	
	//  colors
	$white: #ffffff;
	$grey: #cccccc;
	$snapp-green: #00d170; -->
