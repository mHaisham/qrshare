<script>
    import { onMount } from "svelte";
    import { fade } from "svelte/transition";

    import { QR } from "../components";
    import { title, subtitle, meta } from "../store";

    onMount(() => {
        title.set(2, "QR");
        subtitle.set(2, "Scan to share");
    });
</script>

<svelte:head>
    <title>QR - qrshare</title>
</svelte:head>

<div class="container" in:fade={{ duration: 100 }}>
    <QR />
    <div class="manual">
        <h4>Manual</h4>
        <p>Enter the following in your favourite browser</p>
        <code>{$meta.ip}</code>
    </div>
</div>

<style>
    .manual {
        text-align: center;

        padding-top: 1rem;
        padding-bottom: 2rem;
        border-top: 1px solid var(--color-divider);
    }

    p {
        margin-bottom: 1rem;
    }
</style>
