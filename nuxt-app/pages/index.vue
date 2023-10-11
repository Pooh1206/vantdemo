<template>
    <div>
		<view class="flex diygw-col-24 flex-direction-column flex-nowrap flex-clz">
			<view class="diygw-col-24 white search-clz">
				<view class="diygw-search">
					<view class="flex1 align-center flex padding-xs radius">
						<text style="color: #555 !important" class="diy-icon-search"></text>
						<input class="flex1" name="search" type="" v-model="search" placeholder="doonungonline" />
					</view>
				</view>
			</view>
		</view>
        <h1>home</h1>
    </div>
</template>

<style lang="scss" scoped>
	.flex-clz {
		z-index: 100;
		background-repeat: no-repeat;
		background-size: cover;
		background-image: url(/static/cytb.png);
		background-position: bottom center;
		height: 110px;
	}
	.search-clz {
		margin-left: 10px;
		border-bottom-left-radius: 50px;
		box-shadow: 0px 2px 3px rgba(23, 178, 138, 0.65);
		overflow: hidden;
		width: calc(100% - 5px - 5px) !important;
		border-top-left-radius: 50px;
		margin-top: 10px;
		border-top-right-radius: 50px;
		border-bottom-right-radius: 50px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.flex10-clz {
		margin-left: 10px;
		border-bottom-left-radius: 10px;
		box-shadow: 1px 1px 3px 1px rgba(154, 154, 154, 0.37);
		z-index: 100;
		overflow: hidden;
		width: calc(100% - 10px - 10px) !important;
		border-top-left-radius: 10px;
		margin-top: 0px;
		border-top-right-radius: 10px;
		border-bottom-right-radius: 10px;
		margin-bottom: 10px;
		margin-right: 10px;
	}
	.flex25-clz {
		padding-top: 5px;
		z-index: 100;
		color: #ffffff;
		font-weight: bold;
		padding-left: 5px;
		font-size: 14px !important;
		padding-bottom: 5px;
		height: 80px;
		padding-right: 5px;
	}
	.flex26-clz {
		padding-top: 8px;
		border-bottom-left-radius: 6px;
		z-index: 100;
		background-size: cover;
		padding-left: 8px;
		padding-bottom: 8px;
		border-top-right-radius: 6px;
		margin-right: 5px;
		margin-left: 5px;
		overflow: hidden;
		flex: 1;
		border-top-left-radius: 6px;
		margin-top: 5px;
		border-bottom-right-radius: 6px;
		background-image: url(/static/916f05db-9c0a-4db3-97a6-168e070847c1.png);
		margin-bottom: 5px;
		padding-right: 8px;
	}
	.text21-clz {
		margin-left: 0px;
		color: #e5e5e5;
		font-size: 11px !important;
		margin-top: 5px;
		margin-bottom: 0px;
		margin-right: 0px;
	}
	.flex27-clz {
		padding-top: 8px;
		border-bottom-left-radius: 6px;
		z-index: 100;
		background-size: cover;
		padding-left: 8px;
		padding-bottom: 8px;
		border-top-right-radius: 6px;
		margin-right: 5px;
		margin-left: 5px;
		overflow: hidden;
		flex: 1;
		border-top-left-radius: 6px;
		margin-top: 5px;
		border-bottom-right-radius: 6px;
		background-image: url(/static/cfe2af9f-9039-49d4-9ab6-47c976712d90.png);
		margin-bottom: 5px;
		padding-right: 8px;
	}
	.text25-clz {
		margin-left: 0px;
		color: #e5e5e5;
		font-size: 11px !important;
		margin-top: 5px;
		margin-bottom: 0px;
		margin-right: 0px;
	}
	.flex28-clz {
		padding-top: 8px;
		border-bottom-left-radius: 6px;
		z-index: 100;
		background-size: cover;
		padding-left: 8px;
		padding-bottom: 8px;
		border-top-right-radius: 6px;
		margin-right: 5px;
		margin-left: 5px;
		overflow: hidden;
		flex: 1;
		border-top-left-radius: 6px;
		margin-top: 5px;
		border-bottom-right-radius: 6px;
		background-image: url(/static/6ae393e9-9d10-4664-a6dd-dab7ebfc6c1d.png);
		margin-bottom: 5px;
		padding-right: 8px;
	}
	.text27-clz {
		margin-left: 0px;
		color: #e5e5e5;
		font-size: 11px !important;
		margin-top: 5px;
		margin-bottom: 0px;
		margin-right: 0px;
	}
	.flex23-clz {
		background-color: #ff3646;
		flex-shrink: 0;
		border-bottom-left-radius: 50px;
		overflow: hidden;
		width: 50px !important;
		border-top-left-radius: 50px;
		border-top-right-radius: 0px;
		border-bottom-right-radius: 0px;
	}
	.image1-clz {
		margin-left: 8px;
		margin-top: 0px;
		margin-bottom: 0px;
		margin-right: 0px;
	}
	.image1-size {
		height: 32px !important;
		width: 32px !important;
	}
	.flex24-clz {
		border: 1px solid #ff3646;
		padding-top: 5px;
		border-bottom-left-radius: 0px;
		overflow: inherit;
		flex: 1;
		padding-left: 10px;
		padding-bottom: 5px;
		border-top-left-radius: 0px;
		border-top-right-radius: 50px;
		border-bottom-right-radius: 50px;
		padding-right: 15px;
	}
	.text13-clz {
		font-weight: bold;
		font-size: 14px !important;
	}
	.flex1-clz {
		padding-top: 10px;
		border-bottom-left-radius: 10px;
		z-index: 100;
		padding-left: 10px;
		padding-bottom: 10px;
		border-top-right-radius: 10px;
		margin-right: 10px;
		margin-left: 10px;
		box-shadow: 1px 1px 3px 1px rgba(154, 154, 154, 0.37);
		overflow: hidden;
		width: calc(100% - 10px - 10px) !important;
		border-top-left-radius: 10px;
		margin-top: 10px;
		border-bottom-right-radius: 10px;
		margin-bottom: 10px;
		padding-right: 10px;
	}
	.image-clz {
		border-bottom-left-radius: 6px;
		overflow: hidden;
		border-top-left-radius: 6px;
		border-top-right-radius: 6px;
		border-bottom-right-radius: 6px;
	}
	.image-size {
		height: 130px !important;
		width: 100px !important;
	}
	.flex3-clz {
		padding-top: 0px;
		z-index: 100;
		flex: 1;
		padding-left: 5px;
		padding-bottom: 0px;
		height: 100px;
		padding-right: 0px;
	}
	.flex6-clz {
		z-index: 100;
		flex: 1;
	}
	.flex4-clz {
		z-index: 100;
	}
	.text4-clz {
		margin-left: 0px;
		color: #ff9e01;
		margin-top: 5px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.text5-clz {
		margin-left: 5px;
		margin-top: 5px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.text9-clz {
		border: 1px solid #17b28a;
		padding-top: 5px;
		border-bottom-left-radius: 20px;
		color: #17b28a;
		padding-left: 10px;
		padding-bottom: 5px;
		border-top-right-radius: 20px;
		margin-right: 5px;
		margin-left: 0px;
		overflow: hidden;
		border-top-left-radius: 20px;
		margin-top: 5px;
		border-bottom-right-radius: 20px;
		margin-bottom: 5px;
		padding-right: 10px;
	}
	.flex5-clz {
		z-index: 100;
	}
	.text7-clz {
		border: 1px solid #0ba1f7;
		padding-top: 3px;
		border-bottom-left-radius: 3px;
		color: #0ba1f7;
		padding-left: 5px;
		padding-bottom: 3px;
		border-top-right-radius: 3px;
		margin-right: 5px;
		margin-left: 0px;
		overflow: hidden;
		border-top-left-radius: 3px;
		margin-top: 0px;
		border-bottom-right-radius: 3px;
		margin-bottom: 0px;
		padding-right: 5px;
	}
	.flex8-clz {
		padding-top: 10px;
		border-bottom-left-radius: 10px;
		z-index: 100;
		padding-left: 10px;
		padding-bottom: 10px;
		border-top-right-radius: 10px;
		margin-right: 10px;
		margin-left: 10px;
		box-shadow: 1px 1px 3px 1px rgba(154, 154, 154, 0.37);
		overflow: hidden;
		width: calc(100% - 10px - 10px) !important;
		border-top-left-radius: 10px;
		margin-top: 10px;
		border-bottom-right-radius: 10px;
		margin-bottom: 10px;
		padding-right: 10px;
	}
	.image3-clz {
		border-bottom-left-radius: 6px;
		overflow: hidden;
		border-top-left-radius: 6px;
		border-top-right-radius: 6px;
		border-bottom-right-radius: 6px;
	}
	.image3-size {
		height: 130px !important;
		width: 100px !important;
	}
	.flex12-clz {
		padding-top: 0px;
		z-index: 100;
		flex: 1;
		padding-left: 5px;
		padding-bottom: 0px;
		height: 100px;
		padding-right: 0px;
	}
	.flex16-clz {
		z-index: 100;
		flex: 1;
	}
	.flex18-clz {
		z-index: 100;
	}
	.text15-clz {
		margin-left: 0px;
		color: #ff9e01;
		margin-top: 5px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.text19-clz {
		margin-left: 5px;
		margin-top: 5px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.text22-clz {
		border: 1px solid #17b28a;
		padding-top: 5px;
		border-bottom-left-radius: 20px;
		color: #17b28a;
		padding-left: 10px;
		padding-bottom: 5px;
		border-top-right-radius: 20px;
		margin-right: 5px;
		margin-left: 0px;
		overflow: hidden;
		border-top-left-radius: 20px;
		margin-top: 5px;
		border-bottom-right-radius: 20px;
		margin-bottom: 5px;
		padding-right: 10px;
	}
	.flex20-clz {
		z-index: 100;
	}
	.text24-clz {
		border: 1px solid #0ba1f7;
		padding-top: 5px;
		border-bottom-left-radius: 3px;
		color: #0ba1f7;
		padding-left: 5px;
		padding-bottom: 5px;
		border-top-right-radius: 3px;
		margin-right: 5px;
		margin-left: 0px;
		overflow: hidden;
		border-top-left-radius: 3px;
		margin-top: 0px;
		border-bottom-right-radius: 3px;
		margin-bottom: 0px;
		padding-right: 5px;
	}
	.flex7-clz {
		padding-top: 10px;
		border-bottom-left-radius: 10px;
		z-index: 100;
		padding-left: 10px;
		padding-bottom: 10px;
		border-top-right-radius: 10px;
		margin-right: 10px;
		margin-left: 10px;
		box-shadow: 1px 1px 3px 1px rgba(154, 154, 154, 0.37);
		overflow: hidden;
		width: calc(100% - 10px - 10px) !important;
		border-top-left-radius: 10px;
		margin-top: 10px;
		border-bottom-right-radius: 10px;
		margin-bottom: 10px;
		padding-right: 10px;
	}
	.image2-clz {
		border-bottom-left-radius: 6px;
		overflow: hidden;
		border-top-left-radius: 6px;
		border-top-right-radius: 6px;
		border-bottom-right-radius: 6px;
	}
	.image2-size {
		height: 130px !important;
		width: 100px !important;
	}
	.flex9-clz {
		padding-top: 0px;
		z-index: 100;
		flex: 1;
		padding-left: 5px;
		padding-bottom: 0px;
		height: 100px;
		padding-right: 0px;
	}
	.flex11-clz {
		z-index: 100;
		flex: 1;
	}
	.flex13-clz {
		z-index: 100;
	}
	.text12-clz {
		margin-left: 0px;
		color: #ff9e01;
		margin-top: 5px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.text14-clz {
		margin-left: 5px;
		margin-top: 5px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.text16-clz {
		border: 1px solid #17b28a;
		padding-top: 5px;
		border-bottom-left-radius: 20px;
		color: #17b28a;
		padding-left: 10px;
		padding-bottom: 5px;
		border-top-right-radius: 20px;
		margin-right: 5px;
		margin-left: 0px;
		overflow: hidden;
		border-top-left-radius: 20px;
		margin-top: 5px;
		border-bottom-right-radius: 20px;
		margin-bottom: 5px;
		padding-right: 10px;
	}
	.flex15-clz {
		z-index: 100;
	}
	.text20-clz {
		border: 1px solid #0ba1f7;
		padding-top: 5px;
		border-bottom-left-radius: 3px;
		color: #0ba1f7;
		padding-left: 5px;
		padding-bottom: 5px;
		border-top-right-radius: 3px;
		margin-right: 5px;
		margin-left: 0px;
		overflow: hidden;
		border-top-left-radius: 3px;
		margin-top: 0px;
		border-bottom-right-radius: 3px;
		margin-bottom: 0px;
		padding-right: 5px;
	}
	.container22243 {
		padding-left: 0px;
		padding-right: 0px;
	}
</style>