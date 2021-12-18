<div id="left">
    <img src="/assets/drawers.jpg" alt="Drawers" />
</div>

<style>
    #left {
        min-width: 350px;
        border-top-left-radius: 10px;
        border-bottom-left-radius: 10px;
        overflow: hidden;
    }
    #left > img {
        /* Es importante */
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
    @media all and (max-width: 1440px) {
        #left {
            min-width: auto;
            border-radius: 0;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
            max-height: 300px;
        }
    }
</style>
