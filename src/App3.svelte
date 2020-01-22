<script>
    let name
    let singer
    let framework
    let gender
</script>

<form>
    <input  type="text" binde:value={name}>
    <hr>
    <select bind:value={singer}>
        <option>Ali</option>
        <option>Veli</option>
        <option>Deli</option>
    </select>
    <hr>
    <input type="checkbox" bind:group={frameworks} value="Svelte"> Svelte
    <input type="checkbox" bind:group={frameworks} value="Vue"> Vue
    <input type="checkbox" bind:group={frameworks} value="React"> React
    <hr>
    <input type="radio" bind:group={gender} value="Woman">Woman
    <input type="radio" bind:group={gender} value="Man">Man
</form>

{name} <br />
{singer} <br />
{framework} <br />
{gender} <br />