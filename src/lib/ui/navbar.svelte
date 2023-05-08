<script lang="ts">
	import { Disclosure, DisclosureButton, DisclosurePanel } from '@rgossiaux/svelte-headlessui';
	import Container from '$lib/ui/container.svelte';
	import Logo from '$lib/assets/logo.svg';
	import WLogo from '$lib/assets/logo-white.svg';
	import { LightSwitch } from '@skeletonlabs/skeleton';

	let leftmenu = [
		{
			label: 'Home',
			href: '/'
		},
		{
			label: 'About',
			href: '/about'
		},
		{
			label: 'Contact',
			href: '/contact'
		}
	];

	let rightmenu = [
		{
			label: 'Archive',
			href: '/archive'
		},
		{
			label: 'Pro Version',
			href: 'https://stablo-pro.web3templates.com/',
			external: true,
			badge: 'new'
		},
		{
			label: 'Download',
			href: 'https://web3templates.com/templates/stablo-minimal-blog-website-template',
			external: true
		}
	];

	let mobilemenu = [...leftmenu, ...rightmenu];
</script>

<Container>
	<nav>
		<Disclosure let:open>
			<div class="flex flex-wrap justify-between md:gap-10 md:flex-nowrap">
				<div
					class="flex-col items-center justify-start order-1 hidden w-full md:flex md:flex-row md:justify-end md:w-auto md:order-none md:flex-1"
				>
					{#each leftmenu as item}
						<a href={item.href}>
							<div
								class="px-5 py-2 text-sm font-medium text-gray-600 dark:text-gray-400 hover:text-blue-500"
							>
								{item.label}
							</div>
						</a>
					{/each}
				</div>

				<div class="flex items-center justify-between w-full md:w-auto">
					<a href="/">
						<div class="w-28 dark:hidden">
							<img src={Logo} alt="Logo" sizes="(max-width: 640px)" />
						</div>
					</a>
                    <a href="/">
						<div  class="hidden w-28 dark:block">
							<img src={WLogo} alt="Logo" sizes="(max-width: 640px)" />
						</div>
					</a>

					<DisclosureButton
						aria-label="Toggle Menu"
						class="px-2 py-1 ml-auto text-gray-500 rounded-md md:hidden focus:text-blue-500 focus:outline-none dark:text-gray-300 "
					>
						{#if open}
							<svg
								class="w-6 h-6 fill-current"
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 24 24"
							>
								<path
									fill-rule="evenodd"
									clip-Rule="evenodd"
									d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828 4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1 1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828 4.829 4.828 4.828z"
								/>
							</svg>
						{:else}
							<svg
								class="w-6 h-6 fill-current"
								xmlns="http://www.w3.org/2000/svg"
								viewBox="0 0 24 24"
							>
								<path
									fill-Rule="evenodd"
									d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
								/>
							</svg>
						{/if}
					</DisclosureButton>
				</div>

                <div class="flex-col items-center justify-start order-2 hidden w-full md:flex md:flex-row md:w-auto md:flex-1 md:order-none">
					{#each rightmenu as item}
						<a href={item.href}>
							<div
								class="px-5 py-2 text-sm font-medium text-gray-600 dark:text-gray-400 hover:text-blue-500"
							>
								{item.label}
							</div>
						</a>
					{/each}
                    
				</div>
    <LightSwitch/>
                
			</div>
			<DisclosurePanel>
				<div class="flex flex-col items-center justify-start order-2 w-full md:hidden">
					{#each mobilemenu as item}
						<a href={item.href}>
							<div
								class="px-5 py-2 text-sm font-medium text-gray-600 dark:text-gray-400 hover:text-blue-500"
							>
								{item.label}
							</div>
						</a>
					{/each}
				</div>
			</DisclosurePanel>
		</Disclosure>
        
	</nav>
</Container>

<!-- <Disclosure let:open>
			 {#if open}
                
           
				<div class="flex flex-wrap justify-between md:gap-10 md:flex-nowrap">
					{#each leftmenu as item}
						<a href={item.href}>
							<div
								class="px-5 py-2 text-sm font-medium text-gray-600 dark:text-gray-400 hover:text-blue-500"
							>
								 {item.label}
							</div>
						</a>
					{/each}
				</div>
			
				<div class="flex flex-col items-center justify-start order-2 w-full md:hidden">
					<DisclosurePanel>
						{#each mobilemenu as item}
							<a href={item.href}>
								<div
									class="px-5 py-2 text-sm font-medium text-gray-600 dark:text-gray-400 hover:text-blue-500"
								>
									{item.label}
								</div>
							</a>
						{/each}
					</DisclosurePanel>
				</div>
		   {/if}	 
		</Disclosure>
  -->
