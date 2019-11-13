# vue-awesome-swiper
错误集

## 错误1
### [Vue warn]: Error in nextTick: "SyntaxError: Failed to execute 'remove' on 'DOMTokenList': The token provided must not be empty."
	[Vue warn]: Error in nextTick: "SyntaxError: Failed to execute 'remove' on 'DOMTokenList': The token provided must not be empty."
	found in
	---> <Swiper>
				 <BannerSwiper> at src/components/BannerSwiper.vue
					 <GoodsList> at src/views/GoodsList.vue
						 <App> at src/App.vue
							 <Root>
	 DOMException: Failed to execute 'remove' on 'DOMTokenList': The token provided must not be empty.
	 Uncaught TypeError: Cannot read property 'swiper' of undefined
 
 
 * ## 解决错误1
		//方法：在离开后，路由切换时执行 swiperName.destroy()销毁。
		destroyed(){
				this.swiper.destroy();
			}
