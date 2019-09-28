## component

### single model
``` html
<MyInput v-model="model" @input="handleUserInput" @update="handleJustValueChange"></MyInput>
```

### multiple model
``` html
<CommonTable v-model="$data.selected" :list.sync="$data.list" @update="handleSelectChange" @update:list="handleListUpdate"></CommonTable>
```


### Model base validation and directive (Bag is vuelidate validation bag)
``` html
<CommonTable v-model="$data.foo" v-bag-message.blur="$v.foo"></CommonTable>
<BagMessage :value="$v.foo"><BagMessage>
```

## model and view

### option
```js
[{
  value:"",
  label:"",
  reference:{}
}]
```
```html
<li v-for="{ value, label } in options" :key="value" :label="label" :value="value"><span>{{ label }}<span><li>
```
