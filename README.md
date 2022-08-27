# Rust lib

这是一个示例项目，指导如何发布自己的 rust 库 到 crates.io

# 设置 crates.io 账号

进入 [crates.io](https://https://crates.io/) 中，点击右上角的 **Log in with Github** ，授权并登录

![image](https://user-images.githubusercontent.com/31512287/187017642-8aa96d85-2533-4887-ba0c-1032452e197c.png)


允许之后，进入 **Account Setings**

![image](https://user-images.githubusercontent.com/31512287/187017667-fd872058-88a5-4256-bf1c-723d40b7cdad.png)

在 Profile 中填写自己的邮箱，并把邮箱验证通过

![image](https://user-images.githubusercontent.com/31512287/187017801-6cab94e2-699f-478a-ab0d-5027a54375cb.png)

再点击 API Tokens，新增一个 Token

![image](https://user-images.githubusercontent.com/31512287/187017675-24fdd946-01d2-449f-99b6-d2e5c0b9e5f9.png)

回到自己的机器上，命令行输入

```shell
cargo login ciozxxxxxxxxxxxxxxx1cDl
```

`ciozxxxxxxxxxxxxxxx1cDl` 是你自己的Token

到此，crates的账号设置就完成了。

# 创建 rust lib 项目

通过以下命令可以创建一个 rust lib 项目

```shell
cargo new rust-lib --lib
```

配置描述信息

```toml
[package]
name = "rust-lib"
version = "0.1.0" # refer to semver
edition = "2021"
description = "A rust lib template that can publish to crates.io"
authors = ["Zerounary <gmail_ilak@163.com>"]
license = "MIT"
keywords = ["lib", "codegen", "template"]
repository = "https://github.com/Zerounary/rust-lib.git"
readme = "README.md"


# See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html

[dependencies]
```

开发和测试完库之后，用下面的命令发布

```shell
cargo publish
```

发布过后的程序，就可以在 crates.io 中查询到

![image](https://user-images.githubusercontent.com/31512287/187017902-d957c9b6-af8f-4a6b-b33a-0bccfaf050b9.png)

当然也可以像其他的第三方库一样，直接复制引用到自己的项目中使用。

![image](https://user-images.githubusercontent.com/31512287/187017903-4ba5900b-0d74-4c76-8d0d-5114c9aecba1.png)

