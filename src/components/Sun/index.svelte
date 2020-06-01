<script>
    export let type;
</script>

<style>
    .sun {
        margin-top: -60px;
        margin-right: -55px;
        transition: all 0.8s;
    }

    .animation-wrapper {
        position: absolute;
    }

    .sunrays {
        opacity: 1;
        transition: all 0.5s;
        animation: spin linear 5s infinite;
        transform-origin: center;
    }

    :global(.sun.partly-cloudy-day) .sunrays,
    :global(.sun.rain) .sunrays {
        opacity: 0;
    }

    :global(.sun.rain) {
        transform: translateX(120px);
    }
    
    @keyframes spin {
        from {
            transform: rotate(0);
        }
        
        to {
            transform: rotate(30deg);
        }
    }
</style>

<div class="sun animation-wrapper {type}">
    <svg class="animation-shape" width="200" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 289.76 289.98">
    	<circle cx="145.11" cy="145.11" r="95.98" fill="#fddf70"/>
    	<path class="sunrays" d="M289.76,140.62v9H259.38v-9ZM0,140.62v9H30.39v-9ZM140.62,30.39h9V0h-9ZM17.2,213.78l4.48,7.76L48,206.35l-4.49-7.77ZM198.59,43.51,206.36,48l15.19-26.32-7.76-4.48ZM21.65,68.64l-4.48,7.77L43.49,91.6,48,83.84ZM213.83,273.11l7.77-4.48-15.2-26.32-7.76,4.48ZM68.68,268.52,76.44,273l15.2-26.32-7.77-4.48Zm199.86-47,4.48-7.76-26.31-15.19-4.49,7.76ZM83.86,48l7.76-4.48L76.43,17.18l-7.77,4.49ZM242.22,83.86l4.48,7.77L273,76.44l-4.48-7.77ZM140.63,290h9V259.6h-9Z" fill="#fddf70"/>
    </svg>
</div>