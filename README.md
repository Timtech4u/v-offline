[![Build Status](https://travis-ci.org/vinayakkulkarni/v-offline.svg?branch=master)](https://travis-ci.org/vinayakkulkarni/v-offline)

# V-Offline :zap:
+ Detect offline & online events for your vue app.

+ This is [on GitHub](https://github.com/vinayakkulkarni/v-offline)  so let me know if I've b0rked it somewhere, give me a star :star: if you like it :beers:

+ Demo here -> [💯 Webpackbin Link](https://goo.gl/Pq6Tky)
## Requirements

* [Vue.js](https://vuejs.org/) 2.x

## :white_check_mark: Install :ok_hand:

```bash
npm install v-offline
// or
yarn add v-offline
```

## :white_check_mark: Usage :mortar_board:

Register the component globally:
```javascript
Vue.component('offline', require('v-offline'));
```
Or use locally
```javascript
import offline from 'v-offline';
```

## :white_check_mark: Example :four_leaf_clover:

```html
<offline v-on:detected-condition="detected">
	<div slot="online">
		Your Online Content!
	</div>
	<div slot="offline">
		Your Offline Content!
	</div>
</offline>
```

```javascript
Vue.component('example-component', {
	data() {
		return {
			state: null,
		}
	},
	methods: {
		detected(e) {
			this.state = e;
		}
	}
});
```
### :white_check_mark: :book: Props

| Name | Type | Default | Required? | Description |
| --- | --- | --- | --- | --- |
| `onlineClass` | String | `ui success message` | No | Styling the `div` which you want to give if you're online. |
| `offlineClass` | String | `ui error message` | No | Styling the `div` which you want to give if you're offline. |

### :white_check_mark: :ear: Events

| Name | Description |
| --- | --- |
| `detected-condition` | Emits an Boolean value which can be used for multiple purposes in your app. |


## NPM :octocat:  

[![NPM](https://nodei.co/npm/v-offline.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/v-offline/)