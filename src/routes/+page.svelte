<script lang="ts">
	const links = [
		{
			title: 'View Ionic Components Demo',
			url: '/components',
			external: false
		},
		{
			title: 'Visit Ionic Showcase app with sourceviewer',
			url: 'https://ionic-svelte.firebaseapp.com/',
			external: true
		},
		{
			title: 'Visit Ionic component docs',
			url: 'https://ionicframework.com/docs/components',
			external: true
		},
		{
			title: 'Visit Svelte Kit docs',
			url: 'https://kit.svelte.dev/docs/introduction',
			external: true
		},
		{
			title: 'Visit Svelte docs',
			url: 'https://svelte.dev/docs',
			external: true
		}
	];
</script>

<ion-page class="ion-page">
	<ion-header>
		<ion-toolbar>
			<ion-title>Home</ion-title>
		</ion-toolbar>
	</ion-header>

	<ion-content class="ion-padding">
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
						<ion-button
							href={link.url}
							target={link.external ? '_new' : undefined}
							fill="outline"
							slot="end"
						>
							View
						</ion-button>
					</ion-item>
				{/each}
			</ion-list>
		</ion-card>
	</ion-content>
</ion-page>
