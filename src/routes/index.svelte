<script>
	import Feature from "../components/Feature.svelte";
	import Why from "../components/Why.svelte";
	import Milestone from "../components/Milestone.svelte";
	import Modal from "svelte-simple-modal";
</script>

<style lang="scss">

</style>

<svelte:head>
	<title>ふらっとプラット</title>
</svelte:head>

<Modal>
	<Feature />
	<Why />
	<Milestone />
</Modal>