<script>
	import Modal from './modal.svelte';

	let showModal = false;
</script>

<body>
    <div>
        <p class="title">一起“放轻松”</p>
    </div>
    <div>   
        <img class="round-img" src="/share_image.png" alt="">
    </div>
    <div class="cover-bg">
        <img class="cover-bg-img" src="/share_bg.png" alt="">
        <img class="cover-bg-text" src="/share_text.png" alt="">
    </div>
    <div class="div-btn">
        <img class="play-btn" src="/share_btn.png" alt="" on:click={() => showModal = true}>
	    <button class="round-btn" on:click={() => showModal = true}>马上体验</button>
    </div>
</body>

{#if showModal}
    <Modal on:close="{() => showModal = false}"/>
{/if}

<style>
    body {
        background-color: black;
        transition: background-color 0.3s;
        height: 100vh;
        text-align: center;
    }
    .title {
        color: white;
        font-size: 14px;
    }
    .round-img {
        width: 271px;
        height: auto;
        margin-top: 70px;
    }
    .cover-bg {
        position: relative;
        margin-top: -60px;
        text-align: center;
    }
    .cover-bg-img {
        width: 100%;
        height: auto;
        position: absolute;
        left: 0;
    }
    .cover-bg-text {
        position: absolute;
        display: block;
        width: 155px;
        height: auto;
        left: 50%;
        transform: translateX(-50%);
        margin-top: 64px;
    }
    .div-btn {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
    }
    .play-btn {
        width: 38px;
        height: 38px;
    }
    .round-btn {
        width: 185px;
        height: 44px;
        background: white;
        border-radius: 23px;
        font-size: 16px;
        font-weight: bold;
        margin-top: 160px;
    }
</style>