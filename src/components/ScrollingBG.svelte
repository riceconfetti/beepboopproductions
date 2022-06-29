<script>
    export let text;
</script>

<div class="bg-text-container">
    <div class="animate-text">
        <span>{text}&nbsp;</span>
        <span>{text}&nbsp;</span>
    </div>
    <div class="animate-text left">
        <span>{text}&nbsp;</span>
        <span>{text}&nbsp;</span>
    </div>
    <div class="animate-text">
        <span>{text}&nbsp;</span>
        <span>{text}&nbsp;</span>
    </div>
    <div class="animate-text left">
        <span>{text}&nbsp;</span>
        <span>{text}&nbsp;</span>
    </div>
</div>



<style lang="scss">
    $font-size: 280px;
    $color-bg: #F9B710;
    $color-dark: #000;
    $color-light: #fff;

    .bg-text-container {
        font-family: Akira Expanded, sans-serif;
        font-weight: 500;
        transform: translateX(-50%);
        left: 50%;
        position: absolute;
        z-index: -999;
    }

    @keyframes text-scrolling {
        0% { transform: translate3d(-100%, 0, 0); }
        100% { transform: translate3d(0%, 0, 0); }
    }

    .animate-text {
        animation: text-scrolling 20s linear infinite;
        will-change: transform;
        width: 5250px;
        opacity: 40%;
        display: block;
        position: relative;
        white-space: nowrap;
        &.left {
             animation-direction: reverse;
         }
    }

    span {
        font-size: $font-size;
        color: transparent;
        -webkit-text-stroke: 2px $color-dark;
        text-transform: uppercase;
        display: inline-block;
        line-height: 0.75;
        min-width: auto;
        font-weight: 800;
    }

    .container {
        padding: 30px;
        max-width: 1000px;
        width: 100%;
        margin: 0 auto;
        .col {
            max-width:600px;
            margin: 0;
        }
    }

    h1 {
        font-size: 90px;
        margin: 0;
    }
    p {
        font-size: 18px;
        font-weight: 200;
        margin: 0;
    }


</style>