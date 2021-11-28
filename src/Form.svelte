<script>
    import {count} from '../stores'


    const addcount = () => {
        count.update((currentCount)=> 
        {
            return (currentCount+1);
        });
    }
</script>

<h1>{$count}</h1>

<button on:click={addcount} > Add Count</button>

<style>
    button {
        padding: 0.75rem 1rem;
        margin: 1rem; 
        background-color: #333;
        color: #fff;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }
</style>