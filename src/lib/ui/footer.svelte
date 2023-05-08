<script>
	import Container from "$lib/ui/container.svelte";

	import { LightSwitch } from '@skeletonlabs/skeleton';
 

</script>

<Container  >
    <div class="text-sm text-center">
      Copyright © {new Date().getFullYear()}  . All
      rights reserved.
    </div>
    <div class="flex justify-center gap-1 mt-1 text-sm text-center text-gray-500 dark:text-gray-600">
      <span>
        {" "}
        Made by{" "}
       
        <a
          href="https://web3templates.com/?ref=stablo-template"
          rel="noopener"
          target="_blank">
          Web3Templates
        </a>
      </span>
      <span>&middot;</span>
      <span>
        {" "}
        <a
          href="https://github.com/web3templates/stablo"
          rel="noopener"
          target="_blank">
          Github
        </a>
      </span>
    </div>
    <div class="flex items-center justify-between mt-2">
      <div class="mt-5">
        <a
          href="https://vercel.com/?utm_source=web3templates&utm_campaign=oss"
          target="_blank"
          rel="noopener"
          class="relative block w-44">
          <!-- <Image
            src={VercelLogo}
            layout="fixed"
            loader={myLoader}
            alt="Powered by Vercel"
            unoptimized={true}
            width="150"
            height="25"
          /> -->
        </a>
      </div>
    </div>
   
  </Container>