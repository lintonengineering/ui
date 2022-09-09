<script>
	import GYTR from '$lib/images/Magenta GYTR.png';

	import { page } from '$app/stores';

	const nav = [
		{ title: 'Settings', path: '/settings' },
		{ title: 'User', path: '/user' }
	];
</script>

<div class="min-h-screen bg-transparent">
	<div
		class="sidebar min-h-screen w-[3.05rem] overflow-hidden border-r border-fuchsia-700 hover:w-56 hover:bg-transparent hover:shadow-md"
	>
		<div class="flex h-screen flex-col justify-between pt-2 pb-6">
			<div>
				<div class="w-max p-2.5">
					<img src={GYTR} class="h-21 w-7" alt="GYTR" />
				</div>
				<ul class="mt-6 space-y-2 uppercase">
					<li class="min-w-max">
						{#each nav as item}
							<a
								class="flex py-2 pr-4 pl-5 bg group items-center space-x-4 rounded-full px-4 text-gray-600"
								class:active={$page.url.pathname === item.path}
								href={item.path}
							>
								<img src={GYTR} alt="gytr" class="h-9 w-3" /><span>{item.title}</span></a
							>
						{/each}
					</li>
				</ul>
			</div>
			<div class="w-max -mb-3 uppercase">
				<a
					href="/settings"
					class="group flex items-center space-x-4 rounded-md px-4 py-3 text-pink-600"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-5 w-5 group-hover:fill-pink-600"
						viewBox="0 0 20 20"
						fill="currentColor"
					>
						<path
							fill-rule="evenodd"
							d="M11.49 3.17c-.38-1.56-2.6-1.56-2.98 0a1.532 1.532 0 01-2.286.948c-1.372-.836-2.942.734-2.106 2.106.54.886.061 2.042-.947 2.287-1.561.379-1.561 2.6 0 2.978a1.532 1.532 0 01.947 2.287c-.836 1.372.734 2.942 2.106 2.106a1.532 1.532 0 012.287.947c.379 1.561 2.6 1.561 2.978 0a1.533 1.533 0 012.287-.947c1.372.836 2.942-.734 2.106-2.106a1.533 1.533 0 01.947-2.287c1.561-.379 1.561-2.6 0-2.978a1.532 1.532 0 01-.947-2.287c.836-1.372-.734-2.942-2.106-2.106a1.532 1.532 0 01-2.287-.947zM10 13a3 3 0 100-6 3 3 0 000 6z"
							clip-rule="evenodd"
						/>
					</svg>
					<span class="group-hover:text-pink-700">Settings</span>
				</a>
			</div>
		</div>
	</div>
</div>
