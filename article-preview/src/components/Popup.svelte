<script lang="ts">
    export let isShareOn;
</script>

<div id="popup" class:visible={isShareOn}>
    <div id="bubble">
        <div id="text">
            <p>SHARE</p>
        </div>
        <div id="icons">
            <img src="/assets/icon-facebook.svg" alt="Facebook Icon" />
            <img src="/assets/icon-twitter.svg" alt="Twitter Icon" />
            <img src="/assets/icon-pinterest.svg" alt="Pinterest Icon" />
        </div>
    </div>
    <div id="arrow" />
</div>

<style>
    #popup {
        position: absolute;
        width: 220px;
        height: 100%;
        top: -70px;
        border-radius: 10px;
        box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.25);
        cursor: default;
        opacity: 0;
        visibility: hidden;
        transition: visibility 0.5s, opacity 0.5s;
    }
    #bubble {
        position: absolute;
        border-radius: 10px;
        background-color: rgb(64, 75, 96);
        padding: 15px 30px;
        display: flex;
        z-index: 1;
    }
    #text {
        margin-right: 10px;
    }
    #text > p {
        color: rgb(143, 158, 181);
        letter-spacing: 4px;
        font-size: 13px;
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
    #arrow {
        position: absolute;
        width: 30px;
        height: 30px;
        background-color: rgb(64, 75, 96);
        transform: translateX(-50%) rotate(45deg);
        box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.25);
        left: 50%;
        top: 50%;
    }
    .visible {
        opacity: 1 !important;
        visibility: visible !important;
    }
    @media all and (max-width: 1440px) {
        #popup {
            display: none;
        }
    }
</style>
