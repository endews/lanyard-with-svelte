<script lang="ts">
    export let id: number;

    import { useLanyard } from "svelte-lanyard";

    const lake = useLanyard(`${id}`)
</script>

<main>
    {#if $lake}
        <p>Hewwo I'm {$lake.discord_user.username}#{$lake.discord_user.discriminator} Nice to meet you :3</p>
    {:else}
        <p>Sorry I'm so shy :( </p>
    {/if}
</main>