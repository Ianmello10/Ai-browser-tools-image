<script lang="ts">
	import { goto } from '$app/navigation';
	import { page } from '$app/stores';

	function goToHome() {
		goto('/');
	}
</script>

{#if $page.url.pathname !== '/'}
	<div class="fixed bottom-4 right-4 z-50">
		<button
			class="btn btn-primary btn-circle btn-lg shadow-lg transition-all duration-300 hover:scale-110 hover:shadow-xl"
			onclick={goToHome}
			aria-label="Go to homepage"
		>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				class="h-8 w-8"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
			>
				<path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
				/>
			</svg>
		</button>
	</div>
{/if}
