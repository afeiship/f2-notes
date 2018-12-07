# line to stack:

```js
var line1_data = [
    {
        x: '2018-12-01',
        y: 1.2
    },
    {
        x: '2018-12-02',
        y: 2.2
    },
    {
        x: '2018-12-03',
        y: 4.3
    }
];

var line2_data = [
    {
        x: '2018-12-01',
        y: 2.2
    },
    {
        x: '2018-12-02',
        y: 3.2
    },
    {
        x: '2018-12-03',
        y: 5.3
    }
];
```


## 多个分组合为一个：
```js
function toStackData(){
    var result = [];
    var id = 0;
    var identity = function(){
        return ++id;
    };

    var line1_typeId = identity();
    var items1 = line1_data.map(item=>{
        item.type = 'type_' + line1_typeId;
        return item;
    });


    var line2_typeId = identity();
    var items2 = line2_data.map(item=>{
        item.type = 'type_' + line2_typeId;
        return item;
    });

    result = [].concat(items1, items2);

}

```