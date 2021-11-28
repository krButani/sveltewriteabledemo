# Writable Store Demo
 Writable Store Demo


## Create Stores.js file

- File Code
```
import { writable } from "svelte/store";
```

## App.svelte code 

```
<script>
	import LoadForm from "./Form.svelte";
</script>

<main>
	<LoadForm/>
</main>
```

## Create Form.svelte

- File Code
```
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
```


![Writable Store Demo](ouput.png)

## How to run Project

- First, Clone the repo.
- install required file for following:
    - npm install
- run command
    - npm run dev
- Goto Browser and type http://localhost:5000