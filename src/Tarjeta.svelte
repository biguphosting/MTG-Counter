<script>
    export let name='';
    export let points;
    export let style='default';
    function increasePoints(){
        points++;
    }

    function decreasePoints(){
        points--;
    }
 
</script>
<div class="uk-card uk-card-{style} uk-width-1-6@m uk-card-small uk-margin-small uk-padding-small">
    <div class="uk-card-header"><h3 class="uk-card-title">{name}</h3></div>
    <div class="uk-card-body uk-heading-small uk-text-center">{points}</div>
    <div class="uk-card-footer uk-text-center">
        <button type="button" class="uk-button uk-button large uk-button-primary" on:click={increasePoints}>+</button>
        <button type="button" class="uk-button uk-button large uk-button-secondary" on:click={decreasePoints}>-</button>
    </div>

</div>