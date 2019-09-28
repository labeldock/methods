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
{{ $v.foo.$dirty && $v.foo.$invalid ? 'Invalid' : 'Valid' }}
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
<li v-for="{ value, label } in options" :key="value" :value="value" :label="label"><span>{{ label }}</span><li>
```

### Variable rendering optinal component
```html
<Tab v-model="$data.tab" @input="handleUserTabChange">
  <Item v-for="{ value, label } in tabOptions" :key="value" :value="value" :label="label"><Item>
</Tab>
    
<MySelect v-model="$data.select" @input="handleUserSelectChange">
  <Item v-for="{ value, label } in selectOptions" :key="value" :value="value" :label="label"><Item>
</MySelect>
```

## Special pattern

### BufferModel

### DynamicRenderedOptionComponent

