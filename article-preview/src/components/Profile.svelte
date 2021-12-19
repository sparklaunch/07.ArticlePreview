<script lang="ts">
    import Popup from "./Popup.svelte";
    import MobilePopup from "./MobilePopup.svelte";
    let isShareOn: boolean = true;
    $: innerWidth = 0;
    $: isMobile = innerWidth <= 1440;
    const closePopup: () => void = () => {
        isShareOn = false;
    };
</script>

<svelte:window bind:innerWidth />
<div id="profile">
    <div id="profile-photo">
        <img src="/assets/avatar-michelle.jpg" alt="Avatar" />
    </div>
    <div id="profile-name">
        <p>Michelle Appleton</p>
        <p>28 Jun 2020</p>
    </div>
    <div
        id="profile-share"
        on:click|self={() => {
            isShareOn = !isShareOn;
        }}
    >
        <img src="/assets/icon-share.svg" alt="Share Icon" />
        <Popup {isShareOn} />
    </div>
    {#if isMobile && isShareOn}
        <MobilePopup on:closePopup={closePopup} />
    {/if}
</div>

<style>
    #profile {
        display: flex;
        align-items: center;
        position: relative;
    }
    #profile-photo {
        margin-right: 20px;
    }
    #profile-photo > img {
        width: 50px;
        border-radius: 50%;
    }
    #profile-name {
        flex-grow: 1;
    }
    #profile-name > p:first-child {
        font-weight: 700;
        color: rgb(0, 0, 30);
        margin-bottom: 5px;
    }
    #profile-name > p:last-child {
        color: rgb(148, 157, 168);
    }
    #profile-share {
        margin-left: 20px;
        min-width: 50px;
        height: 50px;
        background-color: rgb(232, 238, 249);
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        cursor: pointer;
    }
    #profile-share > img {
        transition: filter 0.3s;
    }
    #profile-share:hover > img {
        filter: invert();
    }
</style>
