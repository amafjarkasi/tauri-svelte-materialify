<script>
	import { Tabs, Tab, TabContent, MaterialApp, AppBar } from 'svelte-materialify';
	import Inner from './Inner.svelte';
	import Outer from './Outer.svelte';
	import Middle from './Middle.svelte';
</script>


<main>
	<div class="container">
	</div>
	<MaterialApp>
		<AppBar flat>
			<span slot="title"> Title </span>
		  </AppBar>
		<Tabs vertical>
		  <div slot="tabs">
			{#each Array(3) as _, i}
			  <Tab>Item {i + 1}</Tab>
			{/each}
		  </div>
		
		  <div class="pa-2">
			  <TabContent>
				<p>
					<Inner />
				</p>
			  </TabContent>
			  <TabContent>
				<p>
					<Outer />
				</p>
			  </TabContent>
			  <TabContent>
				<p>
					<Middle />
				</p>
			  </TabContent>
		  </div>
		</Tabs>
		</MaterialApp>
</main>

