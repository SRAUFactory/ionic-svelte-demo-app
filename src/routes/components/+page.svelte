<script lang="ts">
</script>

<ion-page class="ion-page">
	<ion-header>
		<ion-toolbar>
			<ion-buttons slot="start">
				<ion-button href="/">Back</ion-button>
			</ion-buttons>
			<ion-title>Ionic Components Demo</ion-title>
		</ion-toolbar>
	</ion-header>

	<ion-content class="ion-padding">
		<ion-card>
			<ion-card-header>
				<ion-card-title>Buttons</ion-card-title>
			</ion-card-header>
			<ion-card-content>
				<ion-button color="primary">Primary</ion-button>
				<ion-button color="secondary">Secondary</ion-button>
				<ion-button color="tertiary">Tertiary</ion-button>
				<br /><br />
				<ion-button color="danger" fill="outline">Danger Outline</ion-button>
				<ion-button color="dark" fill="clear">Clear Button</ion-button>
			</ion-card-content>
		</ion-card>

		<ion-card>
			<ion-card-header>
				<ion-card-title>Badges</ion-card-title>
			</ion-card-header>
			<ion-card-content>
				<ion-badge color="primary">Primary</ion-badge>
				<ion-badge color="secondary">Secondary</ion-badge>
				<ion-badge color="success">Success</ion-badge>
				<ion-badge color="warning">Warning</ion-badge>
				<ion-badge color="danger">Danger</ion-badge>
			</ion-card-content>
		</ion-card>

		<ion-card>
			<ion-card-header>
				<ion-card-title>Controls</ion-card-title>
			</ion-card-header>
			<ion-card-content>
				<ion-list>
					<ion-item>
						<ion-toggle justify="space-between">Enable Notifications</ion-toggle>
					</ion-item>
					<ion-item>
						<ion-checkbox justify="space-between">Accept Terms and Conditions</ion-checkbox>
					</ion-item>
				</ion-list>
			</ion-card-content>
		</ion-card>

		<ion-card>
			<ion-card-header>
				<ion-card-title>Forms (Inputs & Selects)</ion-card-title>
			</ion-card-header>
			<ion-card-content>
				<ion-list>
					<ion-item>
						<ion-input label="Name" label-placement="stacked" placeholder="Enter your name"
						></ion-input>
					</ion-item>
					<ion-item>
						<ion-select label="Favorite Fruit" label-placement="stacked" placeholder="Select one">
							<ion-select-option value="apple">Apple</ion-select-option>
							<ion-select-option value="banana">Banana</ion-select-option>
							<ion-select-option value="orange">Orange</ion-select-option>
						</ion-select>
					</ion-item>
				</ion-list>
			</ion-card-content>
		</ion-card>
	</ion-content>
</ion-page>
