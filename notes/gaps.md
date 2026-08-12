
---
### This для переменных

```
var a = 'BFE'
let b = 'bigfrontend'
console.log(this.a)
console.log(this.b)
```
---
### Вонючие эти == и ===

```
console.log([0] == '') //false
console.log([0] == 0) //true
```

слева будет object, а справа строка или число, оператор == приводит к одному формату
и [0] он будет приводить с помощью toString 
во втором случае строку сравнивают с числом и строку приводят к числу и получается true
---
### Array.push 
```
const a = [1,2,3]
const b = a.push(4)
console.log(a) // [1,2,3,4]
console.log(b) // 4
```

будет ошибка, так как push возвращает длину массива в который пушит
не знал про это
то есть ошибка будет еще на const c = b.push(5), так как нельзя делать 4.push(5)
---
### Constructor 
```
function A() {
  this.dev1 = 'BFE'
  this.dev2 = 'dev'
  return {
    dev1: 'bigfrontend'
  }
}
const a = new A()
console.log(a.dev1) // "bigfrontend"
console.log(a.dev2) // undefined
```
когда используют new, то function используется как конструктор
