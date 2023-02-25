# 3body-lang

[![License](https://img.shields.io/badge/license-MIT%20License-blue.svg)](https://opensource.org/licenses/MIT)
[![Package version](https://img.shields.io/crates/v/three_body_lang.svg)](https://crates.io/crates/three_body_lang)
[![Workflow](https://img.shields.io/github/actions/workflow/status/rustq/3body-lang/CI.yml?branch=main)](https://github.com/rustq/3body-lang/actions)


三体编程语言 Three Body Language written in Rust

Playground: [https://rustq.github.io/3body-lang/](https://rustq.github.io/3body-lang/)

Base on [monkey-lang](https://github.com/wadackel/rs-monkey-lang)

## Try 3body-lang

### With REPL

![carbon](https://user-images.githubusercontent.com/11075892/218237230-18000cfe-8db1-4bf7-979d-a11695039f35.png)

### With Runtime

![carbon-2](https://user-images.githubusercontent.com/11075892/221342321-3f12fe35-df54-45a4-9b20-c9a57681ff64.png)


### With Online Playground

![playground](https://user-images.githubusercontent.com/11075892/218256821-376b9f89-46f7-40b2-9dcd-00baafa31891.png)

Working with Wasm!! 主很在乎 👏🏻

Playground: [https://rustq.github.io/3body-lang/](https://rustq.github.io/3body-lang/)

## Syntax overview

### Variable bindings

##### Format

```
给 <identifier> 以 <expression>;
```

##### Example

```rust
给 岁月 以 "文明";

给 时光 以 "生命";
```

### Operators

##### 前进(+)运算符

```rust
给 自然选择 以 0;

自然选择 前进 4

// > 4
```

##### 降维(-)运算符

```rust
给 宇宙 以 { "维度": 10 };

宇宙["维度"] 降维 7

// > 3
```

### Boolean

```rust
这是计划的一部分

// > true
```

```rust
主不在乎

// > false
```

### Function

##### Format

```
法则 (<parameter one>, <parameter two>, ...) { <block statement> };
```

##### Example

```rust
给 黑暗森林 以 法则() {
    给 基本公理 以 ["生存是文明的第一需要", "文明不断增长和扩张，但宇宙中的物质总量保持不变"];
    基本公理
}

黑暗森林()
```

## Built-in Functions

### Print

##### Format

```
广播(<arg1>, <arg2>, ...): void
```

##### Example

```rust
给 三体世界坐标 以 "半人马星系";

广播(三体世界坐标);

// > "半人马星系"
```

### Sleep

##### Format

```
冬眠(<arg1>): void
```

##### Example

```rust
冬眠(1000);
```

### Clear

##### Format

```
二向箔清理(): void
```

##### Example

```rust
二向箔清理();
```

### Exit

##### Format

```
破壁(): void
```

##### Example

```rust
破壁();
```

## Summary

|Monkey|3body-lang|Explanation|
|---|---|---|
|let|给|"give"|
|=|以|"as"|
|+|前进|"go forward"|
|-|降维|"dimension reduction"|
|true|这是计划的一部分|"It's part of the plan."|
|false|主不在乎|"The Lord doesn't care."|
|fn|法则|"rule"|
|print|广播|"broadcast"|
|sleep|冬眠|"hibernation"|
|clear|二向箔清理|"two-way foil cleaning"|
|exit|破壁|"break the wall"|

## Development

```bash
$ git clone https://github.com/rustq/3body-lang.git

$ cd 3body-lang

$ make repl
```

```
$ ./target/debug/runtime ./example/macroatom.3body
```

```
$ make build_wasm
```

```
$ make test
```

有更多建议和想法 💡

Create issues: [issues](https://github.com/rustq/3body-lang/issues)

## License

[MIT](https://opensource.org/licenses/MIT)
