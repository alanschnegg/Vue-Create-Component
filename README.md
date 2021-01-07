# Vue-Create-Component  
CLI util for create Vue js component made in bash  

Greatly inspired by [vue-generate-component](https://www.npmjs.com/package/vue-generate-component), but there were some things I didn't like, so I decided to do it in my own way  

## Installation

First, you'll need to clone the repository into the folder you want  
```
git clone https://github.com/alanschnegg/Vue-Create-Component Folder
```
*Folder is the path to the folder you want to clone*

Now that you have the script you are going to need to be able to access it from anywhere  
For that, you will add the following line to your bashrc or whatever you use  
```
export PATH=$PATH:Path_folder/Vue-Create-Component
```  
*Path_folder is the exact path to the folder where you cloned before*  

And that's it ! Now you should able to use it anywhere you are !  


## Usage
```
vcc --help
```

### Create a multiple files component
```
vcc -m Component
```

It will create a directory named "Component" with in it 4 files:

**Component.js**
```
export default {
    name: 'Component',
    props: [],
    mounted() {},
    data() {
        return {};
    },
    methods: {},
    computed: {}
}
```

**Component.html**
```
<section class="Component">
    <h1>Component Component</h1>
</section>
```

**Component.scss**
```
.Component {
}
```

**Component.vue**
```
<template src="./Component.html" lang="html"></template>
<script src="./Component.js" lang="js"></script>
<style src="./Component.scss" scoped lang="scss"></style>
```  

---------------------------

### Create a single files component
```
vcc -s Component
```

It will create a file named "Component.vue":
```
<template lang="html">
    <section class="Component">
        <h1>Component Component</h1>
    </section>
</template>

<script lang="js">
    export default {
        name: 'Component',
        props: [],
        mounted() {},
        data() {
            return {};
        },
        methods: {},
        computed: {}
    }
</script>

<style scoped lang="scss">
    .Component {
    }
</style>
```  

---------------------------------

### Others options

You can create several components at the same time
```
vcc -s(or -m) Component1 Component2 Component3
```  

If you don't precise the type of component you want, the script will ask you which
```
$> vcc Component
Multiple / single file (m/s): 
```

It also works in the other way
```
$> vcc -s
Component name: 
```  

And if you are too lazy to use arguments, the script will ask them for you
```
$> vcc
Component name: 
Multiple / single file (m/s):
```  
