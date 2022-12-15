<script>
    import init, { add} from "../../wasm/pkg/rust.js"
    let cumulative = 0

    const add5 = () => {
        const n = add(cumulative, 5)
        cumulative = n
    }
    

</script>

<div>
    <h3>{cumulative}</h3>
    <button on:click={add5}>+ 5</button>
</div>