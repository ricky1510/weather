<script>
    import moment from 'moment';
    export let timestamp;
    const momentDate = moment.unix(timestamp);
</script>

<span class="day__button">
    <span class="date__text">{momentDate.format('MMM DD')}</span>
    <span class="day__text">{momentDate.format('dddd')}</span>
</span>