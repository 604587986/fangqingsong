<script>
    import { createEventDispatcher, onDestroy } from 'svelte';

    const dispatch = createEventDispatcher();
    const close = () => {
		window.location.href = "itms-apps://itunes.apple.com/app/id1605434304";
		dispatch('close');
	};

    let modal;
</script>

<div class="modal-background" on:click={close}></div>

<div class="modal" role="dialog" aria-modal="true" bind:this={modal}>
	<img class="modal-image" src="/share_dialog_bg.png" alt="">
	<p class="modal-title">恭喜 !</p>
	<p class="modal-content">恭喜你获得新用户专享<br><span class="modal-content-white">30天</span>无限体验卡</p>
	<!-- svelte-ignore a11y-autofocus -->
	<button class="modal-btn" autofocus on:click={close}>确定</button>
</div>

<style>
	.modal-background {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0,0,0,0.3);
	}
	.modal {
		position: absolute;
		left: 50%;
		top: 50%;
		width: calc(100vw - 5em);
		max-width: 32em;
		max-height: calc(100vh - 5em);
		overflow: auto;
		transform: translate(-50%,-50%);
		border-radius: 1em;
		background: rgba(55, 53, 57, 1);
	}
	.modal-image {
		width: 100%;
		height: auto;
	}
	.modal-title {
		color: white;
		font-size: 26px;
		font-weight: 500;
		line-height: 10px;
		text-align: center;
	}
	.modal-content {
		color: #CBCBCB;
		font-size: 16px;
		text-align: center;
	}
	.modal-content-white {
		color: white;
		font-size: 16px;
		font-weight: 500;
	}
	.modal-btn {
        width: 92%;
        height: 44px;
        background: white;
        border-radius: 23px;
        font-size: 16px;
        font-weight: bold;
        margin-top: 20px;
		margin-left: 4%;
    }
</style>