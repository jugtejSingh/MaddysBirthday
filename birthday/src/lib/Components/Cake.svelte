<script>
</script>

<div class="Cake">
    <div class="Plate"></div>
    <div class="Layer Layer1"></div>
    <div class="MiddleIcing MiddleIcing1"></div>
    <div class="Layer Layer2"></div>
    <div class="MiddleIcing MiddleIcing2"></div>
    <div class="Layer Layer3"></div>
    <div class="Icing"></div>
    <div class="Strawberry"></div>
    <div class="Strawberry2"></div>
    <div class="Strawberry3"></div>
    <div class="Strawberry4"></div>
    <div class="Strawberry5"></div>
    <div class="Icing2"></div>
    <div class="Icing3"></div>
    <div class="CandleStick"></div>
    <div class="Flame"></div>
</div>

<style>
    .Cake {
        position: relative;
    }
    .Plate {
        position: absolute;
        left: 0;
        right: 0;
        border-radius: 50%;
        width: 20rem;
        height: 8rem;
        background: #ccc;
        z-index: 0;
        box-shadow:
            0 16px 0 #e0dede,
            0 10px 80px rgba(0, 0, 0, 0.5);
    }
    .Layer {
        border-radius: 50%;
        width: 16rem;
        height: 8rem;
        background: #553c13;
        box-shadow:
            0 0.1rem 0 #553c13,
            0 0.2rem 0 #553c13,
            0 0.3rem 0 #553c13,
            0 0.4rem 0 #553c13,
            0 0.5rem 0 #553c13,
            0 0.6rem 0 #553c13,
            0 0.7rem 0 #553c13,
            0 0.8rem 0 #553c13,
            0 0.9rem 0 #553c13,
            0 1rem 0 #553c13;
    }
    .Layer1 {
        position: absolute;
        left: 2rem;
        top: -2rem;
        z-index: 1;
    }
    .Layer2 {
        position: absolute;
        left: 2rem;
        top: -4rem;
        z-index: 3;
    }
    .Layer3 {
        position: absolute;
        left: 2rem;
        top: -6rem;
        z-index: 5;
    }
    .MiddleIcing {
        border-radius: 50%;
        width: 16rem;
        height: 8rem;
        background: #f0e4d0;
        box-shadow:
            0 0.1rem 0 #f0e4d0,
            0 0.2rem 0 #f0e4d0,
            0 0.3rem 0 #f0e4d0,
            0 0.4rem 0 #f0e4d0,
            0 0.5rem 0 #f0e4d0,
            0 0.6rem 0 #f0e4d0,
            0 0.7rem 0 #f0e4d0,
            0 0.8rem 0 #f0e4d0,
            0 0.9rem 0 #f0e4d0,
            0 0.1rem 0 #f0e4d0;
    }
    .MiddleIcing1 {
        position: absolute;
        left: 2rem;
        top: -3.6rem;
        z-index: 2;
    }
    .MiddleIcing2 {
        z-index: 4;
        position: absolute;
        left: 2rem;
        top: -5.6rem;
    }
    .Icing {
        border-radius: 50%;
        width: 16rem;
        height: 8rem;
        background: #f0e4d0;
        box-shadow:
            0 0.1rem 0 #f0e4d0,
            0 0.2rem 0 #f0e4d0,
            0 0.3rem 0 #f0e4d0,
            0 0.4rem 0 #f0e4d0,
            0 0.5rem 0 #f0e4d0,
            0 0.6rem 0 #f0e4d0,
            0 0.7rem 0 #f0e4d0,
            0 0.8rem 0 #f0e4d0,
            0 0.9rem 0 #f0e4d0,
            0 1rem 0 #f0e4d0;
        position: absolute;
        left: 2rem;
        top: -8rem;
        z-index: 5;
    }
    .Icing2 {
        border-radius: 50%;
        width: 7rem;
        height: 6rem;
        background: #f0e4d0;
        position: absolute;
        left: 7rem;
        top: -3rem;
        z-index: 6;
    }
    .Strawberry {
        border-radius: 50%;
        width: 1rem;
        height: 1rem;
        background: lightcoral;
        position: absolute;
        left: 7rem;
        top: -3rem;
        z-index: 6;
    }
    .Strawberry2 {
        border-radius: 50%;
        width: 1rem;
        height: 1rem;
        background: lightcoral;
        position: absolute;
        left: 4rem;
        top: -6rem;
        z-index: 6;
    }
    .Strawberry3 {
        border-radius: 50%;
        width: 1rem;
        height: 1rem;
        background: lightcoral;
        position: absolute;
        left: 15rem;
        top: -3rem;
        z-index: 6;
    }
    .Strawberry4 {
        border-radius: 50%;
        width: 1rem;
        height: 1rem;
        background: lightcoral;
        position: absolute;
        left: 13rem;
        top: -7rem;
        z-index: 6;
    }
    .Strawberry5 {
        border-radius: 50%;
        width: 1rem;
        height: 1rem;
        background: lightcoral;
        position: absolute;
        left: 3rem;
        top: -3rem;
        z-index: 6;
    }

    .Icing3 {
        border-radius: 50%;
        width: 2.1rem;
        height: 3rem;
        background: #f0e4d0;
        position: absolute;
        left: 16rem;
        top: -3.2rem;
        z-index: 7;
    }
    .CandleStick {
        position: absolute;
        left: 9rem;
        top: -9rem;
        width: 1.6rem;
        border-radius: 100% / 10%;
        height: 5.4rem;
        background: red;
        z-index: 7;
    }
    .Flame {
        position: absolute;
        left: 9rem;
        top: -11.5rem;
        width: 1.6rem;
        height: 2.4rem;
        background: orange;
        border-radius: 10px 10px 10px 10px / 25px 25px 10px 10px;
        z-index: 8;
        animation: flicker 3s ease-in-out alternate infinite;
        box-shadow: 0 0.2rem 2rem 10px rgba(255, 165, 0, 0.5);
    }
    @keyframes flicker {
        0% {
            transform: skewX(5deg);
        }
        20% {
            transform: skewX(0deg);
        }
        40% {
            transform: skewX(-5deg) scale3d(110%, 110%, 110%);
        }
        60% {
            transform: skewX(5deg);
        }
        80% {
            transform: skewX(0deg);
        }
        1000% {
            transform: skewX(5deg) scale3d(110%, 110%, 110%);
        }
    }
</style>
