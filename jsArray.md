#Stack vs queue
둘다 자료구조에서 어떻게 데이터를 메모리에 할당하고 인출할 것인지에 대한 방법론 

1.Stack -  Last in First out 으로 먼저 넣은 것이 나중에 나오는 구조 
박스에 물건을 넣고 마지막에 넣은 것을 꺼내는 것과 같음 
ex. undo를 할 때, 용이한 구조 
push / pop

2.Queue - First in First out으로 먼저 넣은 것이 먼저 나오는 구조 
일렬로 줄서있다가 그대로 입장하는 것과 같음 
push / shift

3.Splice - 배열에서 특정 부분을 잘라서 삭제한뒤, 다른 데이터로 치환할 때 씀 
```
array.splice(index num, 추출할 요소 갯수, ...치환할 데이터 값 ) 
ex.
var data = ['a','b','c','d','e']
console.log(data.splice(3,2,'h'));  // 치환할 데이터 값 전과 후의 갯수는 다를 수 있다. 
-> result : data = ['a','b','c','h'];
```

#Array 함수에서 사용자 지정 함수로 처리 가능한 콜백 함수 : for each/map/some/filter 
1. for each 
```
var data = [1,2,3,4]; 
data.forEach(function(value, index, array){
    console.log(value*value);
});

results: 1,4,9,16;
```
2. map 
```
var testArray = ['a','b','c','d']; 
undefined
var newArray = testArray.map(function(item, index, array){
    return item + "NEW";
});
undefined
console.log(testArray);
["a", "b", "c", "d"]

console.log(newArray);
["aNEW", "bNEW", "cNEW", "dNEW"]
```
3. Some : 조건에 해당하는 부분이 나오면 멈추고 true/false 반환 
```
testArray.some(function(value, index, array){
    console.log(index +"번째 요소" + value);
    return !!~value.search("b");
});
0번째 요소a
1번째 요소b
true
```
4. Filter : 조건에 해당하는 부분이 나오면 치환 
```
var againArray = testArray.filter(function(value, index, array){
    return value.search(/[c]+/);
});

console.log(againArray);
["a", "b", "d"]
```
