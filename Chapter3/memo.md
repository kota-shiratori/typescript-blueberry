- interface宣言で扱えるのはオブジェクト型だけ
- ほとんどの場合、interface宣言はType文で代用可能（2014年以前はType文が存在せずinterface宣言のみ利用可能だったという歴史的背景がある）
- インデックスシグネチャ：「どんな名前のプロパティも受け入れる」という性質のオブジェクト型を記述することができる
```TypeScript:index.ts
type PriceData = {
    [key: string]: number;
}
```
- インデックスシグネチャは古い機能である→推奨できない

- オプショナルなプロパティ?
```TypeScript:index.ts
type MyObj = {
    foo: boolean;
    bar: boolean;
    baz?: boolean;
}
```

- 読み取り専用のプロパティ readonly
```TypeScript:index.ts
type MyObj = {
    readonly foo: number;
}
```
- typeofキーワード：typeof 変数名　でその変数が持つ型を表す
- 型推論の結果を型として抽出・再利用したい場合にtypeofは効果的

- 部分型：２つの型の互換性を表す概念
```TypeScript:index.ts
type FooBar = {
    foo: string;
    bar: number;
}
type FooBarBaz = {
    foo: string;
    bar: number;
    baz: boolean;
}

const obj: FooBarBaz = {
    foo: "hi;
    bar: 1;
    baz: false;
};
const obj2: Foobar = obj;
```

- プロパティの包含関係
```TypeScript:index.ts
type Animal = {
    age: number;
}
type Human = {
    age: number;
    name: string;
}
```