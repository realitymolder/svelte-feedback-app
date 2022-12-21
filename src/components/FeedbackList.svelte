<script lang="ts">
    import { FeedbackStore } from "../stores";
    import FeedbackItem from "./FeedbackItem.svelte";
    let feedback = [];

    FeedbackStore.subscribe((data) => feedback = data);


</script>

{#each feedback as fb (fb.id)}
<FeedbackItem item={fb} on:delete-feedback/>
{/each}