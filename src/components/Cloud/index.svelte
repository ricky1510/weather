<script>
    export let type;
</script>

<style>
    .cloud {
        margin-top: 30px;
        margin-right: 45px;
        transition: all 0.8s;
        z-index: 20;
    }

    .cloud-shape {
        animation: drift linear 15s infinite;
    }
    .raindrop1-shape {
        animation: rain linear 1s infinite;
        position: absolute;
        left: 50%;
        top: 100%;
        margin-top: 5px;
    }
    .raindrop2-shape {
        animation: rain linear 0.8s infinite;
        position: absolute;
        left: 60%;
        top: 100%;
        margin-top: 4px;
    }
    .raindrop3-shape {
        animation: rain linear 0.9s infinite;
        position: absolute;
        left: 30%;
        top: 100%;
        margin-top: 4px;
    }
    .raindrop4-shape {
        animation: rain linear 0.7s infinite;
        position: absolute;
        left: 40%;
        top: 100%;
        margin-top: 4px;
    }
    .raindrop5-shape {
        animation: rain linear 0.7s infinite;
        position: absolute;
        left: 50%;
        top: 100%;
        margin-top: 4px;
    }

    :global(.cloud.clear-day) {
        transform: translateX(-200px);
        opacity: 0;
    }

    :global(.cloud.partly-cloudy-day) .raindrop {
        display: none;
    }

    @keyframes rain {
        0% {
            transform: translateY(0px);
            opacity: 1;
        }
        100% {
            opacity: 0;
            transform: translateY(100px);
        }
    }

    @keyframes drift {
        0% {
            transform: translateX(0px);
        }
        25% {
            transform: translateX(-20px);
        }
        50% {
            transform: translateX(0px);
        }
        75% {
            transform: translateX(20px);
        }
        100% {
            transform: translateX(0px);
        }
    }
</style>

<div class="cloud animation-wrapper {type}">
    <svg class="cloud-shape animation-shape" width="170" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 144.74 86.02">
        <path d="M143.74,64.64a20.38,20.38,0,0,0-20.38-20.39,20.67,20.67,0,0,0-2.74.21A47,47,0,0,0,30.83,28.74c-.55,0-1.11,0-1.67,0A28.16,28.16,0,0,0,28,85v0h96.59V85A20.37,20.37,0,0,0,143.74,64.64Z" fill="#fff" stroke="#51159b" stroke-miterlimit="10" stroke-width="2"/>
    </svg>
    <svg width="10" class="raindrop raindrop1-shape" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25.47 39.92">
        <path d="M24,21.26h0L12.77,0,1.56,21.07l-.07.13,0,.06h0a12.74,12.74,0,1,0,24,5.92A12.57,12.57,0,0,0,24,21.26Z" fill="#80d2ea"/>
    </svg>
    <svg width="8" class="raindrop raindrop2-shape" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25.47 39.92">
        <path d="M24,21.26h0L12.77,0,1.56,21.07l-.07.13,0,.06h0a12.74,12.74,0,1,0,24,5.92A12.57,12.57,0,0,0,24,21.26Z" fill="#80d2ea"/>
    </svg>
    <svg width="9" class="raindrop raindrop3-shape" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25.47 39.92">
        <path d="M24,21.26h0L12.77,0,1.56,21.07l-.07.13,0,.06h0a12.74,12.74,0,1,0,24,5.92A12.57,12.57,0,0,0,24,21.26Z" fill="#80d2ea"/>
    </svg>
    <svg width="9" class="raindrop raindrop4-shape" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25.47 39.92">
        <path d="M24,21.26h0L12.77,0,1.56,21.07l-.07.13,0,.06h0a12.74,12.74,0,1,0,24,5.92A12.57,12.57,0,0,0,24,21.26Z" fill="#80d2ea"/>
    </svg>
    <svg width="9" class="raindrop raindrop5-shape" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 25.47 39.92">
        <path d="M24,21.26h0L12.77,0,1.56,21.07l-.07.13,0,.06h0a12.74,12.74,0,1,0,24,5.92A12.57,12.57,0,0,0,24,21.26Z" fill="#80d2ea"/>
    </svg>
</div>