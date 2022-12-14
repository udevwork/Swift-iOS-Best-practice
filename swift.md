## Замыкание

Замыкание - исполняемый фрагмент кода, который захватывает значения из констекста. Экземпляр функции, который имеет доступ к определенному контексту и / или фиксирует определенные значения и может быть вызвана позже.

Счетчик и замыкание существуют в одной и той же области. Замыкание может считывать текущее значение счетчика

```swift
var counter = 1 // значимый тип

let myClosure = {
    print(counter)
}

myClosure() // prints 1
counter += 1
myClosure() // prints 2
```

Захват значения counter в момент создания замыкания:

```swift
var counter = 1

let myClosure = { [counter] in
    print(counter)
}

myClosure() // prints 1
counter += 1
myClosure() // prints 1
```
