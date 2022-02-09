# Map

```
ES6提出的一种新的新的集合类型，特点是键值对映射。键值可以是js中任意的数据类型，通过new Map()来创建一个map
```

## Map的API

### 1.1	set 和 get方法

```
通过set方法更新或者新增键值对，返回更新后的映射，所以set方法可以链式调用；
通过get方法获取指定键对应的值,传入不存在的key，返回undefined；
const map = new Map();
map.set('k1','v1').set('k2','v2')===>{k1=>v1,k2=>v2}
map.set('k1',v3)===>{k1=>v3,k2=>v2}
map.get('k2')===>v2
```

### 1.2	clear和delete方法

```
通过clear方法清空map
通过delete方法删除指定的键值对并返回删除结果（true和false）
const map = new Map();
map.set('k1','v1').set('k2','v2')
map.delete('k1')===>true
map.delete('v1')===>false
map.clear()===>{}
```

### 1.3	has方法

```
通过has方法来判断映射是否包含键值对
map.has('k1')====>true
map.has('v1')====>false
```

### 1.4	size

```
该属性返回映射内存在多少键值对
const map = new Map([[1,2],[2,3],[3,4]])
map.size=== 3 //true
```

### 1.5	forEach和entries方法

```
映射的遍历方法
entries方法返回键值对的迭代器
forEach方法接收一个回调函数，可以在该函数中获取当前遍历的键值
map.forEach((k,v)=>{
	console.log(k,v);
})//1,2 2,3 3,4
```

# WeakMap

```
弱映射，API与Map的API相同，数据结构也是键值对存储，但是与Map不同的是，WeakMap的键只能是Object（继承自Object）类型
```

# Map与Object的区别（何时使用Map）

1. 存储结构都是键值对结构，键与值的类型为js的任意类型
2. 存储：相同的内存空间，Map可以存储的键值对比Object存储的多
3. 添加数据：两者插入数据的性能相差不大，Map性能比Object略高（当涉及到大量数据插入时，可以选用Map）
4. 查询性能：两者查询数据的性能相差不大，但是少量键值对存储的情况下进行查询，Object的查询性能要高于Map，大量键值对存储的查询，Map的性能更优
5. 删除性能：删除键值对时，Map的性能要远高于Object，涉及大数据量键值对的删除时，Map更优
