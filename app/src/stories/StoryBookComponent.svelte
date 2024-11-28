<script>
    /**
     * @typedef {Object} Props
     * @property {string} prop1 Test string prop
     * @property {string} prop2 Test string prop
     * @property {boolean} logged The boolen prop
     */

    /** @type {Props} */
    const { prop1, prop2, logged } = $props();
</script>

{#if logged}
    <div>{prop1} {prop2}</div>
{:else}
    <div>{prop2} {prop1}</div>
{/if}