<template>
	<div class="flex justify-center gap-4 font-semibold text-xl">
		<div class="flex items-center justify-end gap-2 w-full">
			<p>You</p>
			<IconMarkX class="w-4 fill-slate-400" />
			<p v-text="store.scores.x" />
		</div>

		<p class="font-bold">-</p>

		<div class="flex items-center gap-2 w-full">
			<p v-text="store.scores.o" />
			<IconMarkO class="w-4 fill-slate-400" />
			<p>Bot</p>
		</div>
	</div>
</template>

<script setup>
import IconMarkX from "@/components/icons/IconMarkX.vue";
import IconMarkO from "@/components/icons/IconMarkO.vue";
import { useGameStore } from "@/stores/game";

const store = useGameStore();
</script>
