# nativescript-facebook-vue-example
Nativescript-facebook plugin with nativescript-vue example

<code>npm install -s nativescript-facebook</code>

Required!

<code>npm run clean</code>

And then:

<code>import * as Facebook from "nativescript-facebook";</code>

In created:

<code>Facebook.init('APP_ID');</code>

And use method:

<code>Facebook.login((err, fbData) => { });</code>
