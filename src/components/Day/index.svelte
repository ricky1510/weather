<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
    export let i;

    function activateDay() {
        dispatch('changeDay', {
            day: i
        });
    }

    import moment from 'moment';
    export let timestamp;
    const momentDate = moment.unix(timestamp);
</script>

<button class="day__button" on:click={activateDay}>
    <span class="date__text">{momentDate.format('MMM DD')}</span>
    <span class="day__text">{momentDate.format('dddd')}</span>
</button>