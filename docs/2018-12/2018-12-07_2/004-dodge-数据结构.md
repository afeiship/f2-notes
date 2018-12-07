# dodge:
> 与 stack 相同

## f2 data:
```js
var data = [
    {
        type: 'type1',
        x: '2018-12-01',
        y: 1.2
    },
    {
        type: 'type1',
        x: '2018-12-02',
        y: 2.2
    },
    {
        type: 'type2',
        x: '2018-12-01',
        y: 4.3
    },
    {
        type: 'type2',
        x: '2018-12-02',
        y: 6.3
    }
];
```

## expect data:
```js
var data = [
    {
        type: 'type1',
        items: [
            { x: '2018-12-01', y: 1.2 },
            { x: '2018-12-02', y: 2.2 }
        ]
    },
    {
        type: 'type2',
        items: [
            { x: '2018-12-01', y: 4.2 },
            { x: '2018-12-02', y: 6.6 }
        ]
    }
]
```
