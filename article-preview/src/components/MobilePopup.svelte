<script lang="ts">
    import { slide } from "svelte/transition";
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
    const clickedHandler: () => void = () => {
        dispatch("closePopup");
    };
</script>

<div id="mobile-popup" transition:slide>
    <div id="share-text">
        <p>SHARE</p>
    </div>
    <div id="icons">
        <img src="/assets/icon-facebook.svg" alt="Facebook Icon" />
        <img src="/assets/icon-twitter.svg" alt="Twitter Icon" />
        <img src="/assets/icon-pinterest.svg" alt="Pinterest Icon" />
    </div>
    <div id="share-button" on:click={clickedHandler}>
        <img src="/assets/icon-share.svg" alt="Share Icon" />
    </div>
</div>

<style>
    #mobile-popup {
        position: absolute;
        background-color: rgb(64, 75, 96);
        width: calc(100% + 80px);
        display: flex;
        align-items: center;
        padding: 30px 40px;
        bottom: -40px;
        left: -40px;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
    }
    #share-text {
        margin-right: 20px;
    }
    #share-text > p {
        color: rgb(128, 141, 165);
        letter-spacing: 5px;
    }
    #icons {
        display: flex;
        align-items: center;
    }
    #icons > img {
        cursor: pointer;
    }
    #icons > img:not(:last-child) {
        margin-right: 15px;
    }
    #share-button {
        display: flex;
        justify-self: end;
        justify-content: center;
        align-items: center;
        width: 36px;
        height: 36px;
        border-radius: 50%;
        background-color: rgb(95, 114, 140);
        margin-left: auto;
        cursor: pointer;
    }
    #share-button > img {
        filter: saturate(0) brightness(3);
    }
</style>
