# Typescript

Source: [The TypeScript Handbook](https://www.typescriptlang.org/docs/handbook)

## Basic Types

### Boolean

```
let someBoolean: boolean = false
```

### Number

```
let someNumber: number = 5;
```

### String

```
let someString: string = "str";
someString = "other";
```

### Array

```
let someArr: number[] = [1, 2, 3];
let someOtherArr: Array<number> = [1, 2, 3];
```

### Tuple

```
let someTuple: [string, number];
someTuple = ["hello"m , 10];
```

### Enum

```
enum Color {
	Red,
	Green,
	Blue
}
let c: Color = Color.Green;
```
### Unknown

```
let notSure: unknown = 4;
```

### Any

```
let looselyTyped: any = "anything";
```

### Void

```
function log(x: any): void { console.log(x) }
```

### Null and Undefined 

```
let u: undefined = undefined;
let n: null = null;
```

### Never

```
function error(): never { throw new Error("err") }
```

### Object 

```
declare function create(o: object | null): void;
```

### Type assertions

```
let someValue: any = "this is a string";

let strLength: number = (someValue as string).length;
let strLength2: number = (<string>someValue).length;
```

## Interfaces

### Basic

```
function fun(obj: { f1: string }) {
 // do something
}

fun({f1: "x", f2: "y"}); // OK
```

```
interface LabeledValue {
  label: string;
}

```

### Optonal properties

```
interface SquareConfig {
  color?: string;
  width?: number;
}
```

### Readonly properties

```
interface Point {
  readonly x: number;
  readonly y: number;
}

let ro: ReadonlyArray<number> = [1, 2, 3, 4];
```

### Function Types

```
interface SearchFunc {
  (source: string, subString: string): boolean;
}
```

### Indexable Types

```
interface StringArray {
  [index: number]: string;
}
```

Note: can be readonly and can have union types for property byt not unassignable types

### Class Types

```
interface ClockInterface {
  currentTime: Date;
  setTime(d: Date): void;
}

class Clock implements ClockInterface {
  currentTime: Date = new Date();
  setTime(d: Date) {
    this.currentTime = d;
  }
  constructor(h: number, m: number) {}
}
```


### Extending Interfaces

```
interface Shape {
  color: string;
}

interface Square extends Shape {
  sideLength: number;
}
```

Other: Hybrid types and Interfaces Extending Classes

















































