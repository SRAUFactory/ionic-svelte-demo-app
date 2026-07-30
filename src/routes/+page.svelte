<script lang="ts">
	const links = [
		{
			title: 'Visit Ionic Showcase app with sourceviewer',
			url: 'https://ionic-svelte.firebaseapp.com/'
		},
		{
			title: 'Visit Ionic component docs',
			url: 'https://ionicframework.com/docs/components'
		},
		{
			title: 'Visit Svelte Kit docs',
			url: 'https://kit.svelte.dev/docs/introduction'
		},
		{
			title: 'Visit Svelte docs',
			url: 'https://svelte.dev/docs'
		}
	];
</script>

<ion-card>
	<ion-card-header>
		<ion-card-subtitle>Great success!!</ion-card-subtitle>
		<ion-card-title>Welcome to your app!</ion-card-title>
	</ion-card-header>

	<ion-card-content>
		Thank you for using this starter. Click buttons below to open these guides (will open in new
		window). Don't forget to open DevTools to see this app in mobile mode. Happy coding!!!
	</ion-card-content>

	<ion-list>
		{#each links as link}
			<ion-item>
				<ion-label>{link.title}</ion-label>
				<ion-button href={link.url} target="_new" fill="outline" slot="end">View</ion-button>
			</ion-item>
		{/each}
	</ion-list>
</ion-card>
