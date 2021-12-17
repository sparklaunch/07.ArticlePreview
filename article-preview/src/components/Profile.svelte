<script lang="ts">
    let isShareOn: boolean = false;
</script>

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
        on:click={() => {
            isShareOn = !isShareOn;
        }}
    >
        <img src="/assets/icon-share.svg" alt="Share Icon" />
    </div>
</div>

<style>
    #profile {
        display: flex;
        align-items: center;
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
        width: 50px;
        height: 50px;
        background-color: rgb(232, 238, 249);
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        transition: filter 0.3s;
    }
    #profile-share:hover {
        filter: invert();
    }
</style>
