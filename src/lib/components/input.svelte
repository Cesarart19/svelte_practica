<script lang="ts"> 
    import debounce  from 'lodash.debounce';
    export let search: string = ''

    const onInputChange = debounce((event: Event) => {
        search = (event.target as HTMLInputElement).value;
    }, 500);
</script>

<input  
    bind:value={search}
    type="text"
    class="block w-80 h-9 px-3 rounded"
    placeholder="enter your search..."
    on:input={onInputChange}
    />