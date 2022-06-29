<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

## Layers

You can customize the initial state of the module from the editor initialization

```js
const editor = grapesjs.init({
 // ...
 layerManager: {
   // ...
 },
})
```

Once the editor is instantiated you can use its API. Before using these methods you should get the module from the instance

```js
const layers = editor.Layers;
```

## Available Events

*   `layer:root` - Root layer changed. The new root component is passed as an argument to the callback.
*   `layer:component` - Component layer is updated. The updated component is passed as an argument to the callback.

## Methods

*   [setRoot][1]
*   [getRoot][2]
*   [getLayerData][3]

[Page]: page.html

[Component]: component.html

## setRoot

Update root layer with another component.

### Parameters

*   `component` **([Component] | [String][4])** Component to be set as root

### Examples

```javascript
const component = editor.getSelected();
layers.setRoot(component);
```

Returns **[Component]** 

## getRoot

Get the current root layer.

### Examples

```javascript
const layerRoot = layers.getRoot();
```

Returns **[Component]** 

## getLayerData

Get layer data from a component.

### Parameters

*   `component` **[Component]** Component from which you want to read layer data.

### Examples

```javascript
const component = editor.getSelected();
const layerData = layers.getLayerData(component);
console.log(layerData);
```

Returns **LayerData** Object containing layer data

## setVisible

Update component visibility

### Parameters

*   `component` **Component** 
*   `value` **[boolean][5]** 

## isVisible

Check if the component is visible

### Parameters

*   `component` **Component** 

Returns **[boolean][5]** 

## setLocked

Update component locked value

### Parameters

*   `component` **Component** 
*   `value` **[boolean][5]** 

## isLocked

Check if the component is locked

### Parameters

*   `component` **Component** 

Returns **[boolean][5]** 

## setName

Update component name

### Parameters

*   `component` **Component** 
*   `value` **[string][4]** 

[1]: #setroot

[2]: #getroot

[3]: #getlayerdata

[4]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String

[5]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean