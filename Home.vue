<template>
  <Page class="page">
    <ActionBar class="action-bar" title="Home"/>

    <StackLayout>
      <Button class="btn btn-primary" @tap="login">Facebook login</Button>
    </StackLayout>

  </Page>
</template>

<script>
	import * as Facebook from "nativescript-facebook";

	export default {
		created() {
			Facebook.init('APP_ID');
		},
		methods: {
			login() {
				Facebook.login((err, fbData) => {
					if (err) {
						alert("Error during login: " + err.message);
					} else {
						console.log(fbData.token);
					}
				});
				
			}
		}
	}
</script>
