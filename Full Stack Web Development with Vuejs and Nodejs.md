- https://vuejs.org/v2/guide/  
- https://vuejs.org/v2/cookbook/  
- https://github.com/vuejs/vue-devtools#vue-devtools
- https://www.coindesk.com/api
- https://vuex.vuejs.org/
- https://vuetifyjs.com/en/getting-started/quick-start
- http://docs.sequelizejs.com/

```
node -v
npm -v
mkdir vue-npm
cd vue-npm
npm init -f
npm install vue --save
```

```
<html>
<body>
		<div id="app">
			{{ message }}
		</div>

		<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
		--OR--
		<script src="node_modules/vue/dist/vue.js"></script>
		
		<script>
			var app = new Vue({
				el: '#app',
				data: {
					message: " Hello Vue"
				}
			});
		</script>
</body>
</html>
```
---
1. **vue cli**
```
npm install -g @vue/cli
vue --version
vue create client
	OR vue ui
cd client
npm run serve
```

**Project Files**
- node_modules - dependencies needed to build a project
- public - files you don't want to run through Webpack
> - index.html
- src - where all the application code goes
> - assets - assets of project like images, fonts
> - components - store building blocks of application
> - App.vue - root component where all the other components are nested within
> - main.js - script file that render the application and mounts it to the DOM
- .gitignore
- package.json

***main.js***
```
import Vue from 'vue'
import App from './App.vue'

Vue.config.productionTip = false

new Vue({
  render: h => h(App),
}).$mount('#app')
```
***index.html***
```
<html>
	<div id="app"></div>
</html>
```

**Single-File Components***  
Global Components Disadvantages: 
- Global definitions
- String templates
- No CSS Support
- No build step  

**Single-File Components**
```
<template>
<script>
<style>
```

***HelloWorld.vue***
```
<template>
	  <div class="hello">
				<h1>{{ msg }}</h1>
	  </div>
</template>

<script>
export default {
	  name: 'HelloWorld',
	  props: {
		msg: String
	  }
	}
</script>

<style scoped>
</style>
```

***App.vue***
```
<template>
	<div id="app">
		<HelloWorld msg="Welcome to Your Vue.js App"/>
	</div>
</template>

<script>
	import HelloWorld from './components/HelloWorld.vue'
	
	export default {
	  name: 'app',
	  components: {
				HelloWorld
	  }
	}
</script>

<style>
</style>
```
---
2. **Axios**
- a promise-based HTTP client
```
npm install --save axios
```
---
3. **Vuex**
```
npm install --save vuex
```
or
```
<script src="https://unpkg.com/vuex@3.1.1/dist/vuex.js"> </script>
<script>
	const store = new Vuex.Store({
		state: {
			count: 0
		},
		mutations: {
			increment: state => state.count++,
			decrement: state => state.count--
		}
	})

	
	var app = new Vue({
		el: '#app',
		computed: {
			count(){
				return store.state.count
			}
		}
	})
</script>
```

**main.js**
```
import Vuex from 'vuex'
Vue.use(Vuex)
```

Core Concepts:
- Vuex is a state management pattern plus library
- Vuex : Vue Components dispatch | **Actions** | commit | **Mutations** |  mutate | **State** | render Vue Components
- State
- Getters
- Mutations
- Actions
- Modules

---
4. **vue-router**
```
npm install --save vue-router
```
**main.js**
```
import VueRouter from  'vue-router'
Vue.use(VueRouter)
```
---
**Playlist**
1. Client: *Vue*
```
mkdir vue-playlist
cd vue-playlist
vue create client
cd vue-playlist
npm install --save vue-router
npm install --save vuetify
npm install --save axios
npm install --save vuex
npm run serve
```
```
material icons
npm install material-design-icons-iconfont -D
```
2. Server: *Express*
```
mkdir server
cd server
npm init -f
npm install --save express
npm install --save body-parser cors morgan
npm install --save jsonwebtoken
npm install --save joi
npm install --save bcrypt-nodejs
npm install --save bluebird
```

* Express
*src/app.js*
```
const express = require('express')
const app= express()
const port=3000

app.get("/", (req, res) => res.send("Helloo World"))
app.listen(port, () => console.log("Your application is listening on ${port} "))

To run: node src\app.js
```
3. Database: *Sequelize*
```
cd server
npm install --save sequelize
npm install --save sqlite3
```


