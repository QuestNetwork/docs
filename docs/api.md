# utilities

## inArray(array,value)

Returns boolean true or false
```javascript
if(<os>.utilities.inArray(array,value)){
 console.log('Hello Universe!')
}
```

## removeFram(array,searchObject)

Removes the object in the array that matches searchObject in at least one field.
```javascript
<os>.utilities.removeFram(array,searchObject)
```

## engine.detect()

Returns a String containing the detected engine. Result can be `browser`, `electron` or `node`.
```javascript
let engine = <os>.utilities.engine.detect();
```

## qr.generate()

Returns a DataUrl containing generated QR Code.
```javascript
let qrDataUrl = <os>.utilities.qr.generate(text);
```


