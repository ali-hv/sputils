# **🛠️ sputils**

sputils is a lightweight command-line utility to scaffold feature-based package structures in a Spring Boot project.

It follows the **package-by-feature** design pattern — organizing code into cohesive feature modules, each containing its own controller, service, entity, repository, DTOs, and mappers.

## **📦 Features**

* Quickly scaffold a new feature module (like Django's startapp)
* Clean, organized folder structure inside your base package
* Easily extensible for future Spring-related CLI commands

## **🚀 Getting Started**

### **1. Clone the repository**

```bash
git clone https://github.com/ali-hv/sputils.git
```

### **2. Install**

Install the **sputils** by running the install script:
```bash
chmod +x install
./install
```

## **⚙️ Usage**

```bash
sputils <command> [options]
```

### **Available Commands:**

#### `startapp <feature-name> [options]`

Scaffold a new feature module with the following structure:

```
src/main/java/com/example/project/<feature-name>/
├── controller/
├── dto/
├── entity/
├── mapper/
├── repository/
└── service/
```

### **Example:**

```bash
sputils startapp user
```

Creates:
```
src/main/java/com/example/project/user/
├── controller/
├── dto/
├── entity/
├── mapper/
├── repository/
└── service/
```

You can also send the --gen-classes argument to create a java stub for each layer:

### **Example:**

```bash
sputils startapp user --gen-classes
```

Creates:
```
src/main/java/com/example/project/user/
├── controller/
|──── UserController.java
├── dto/
|──── UserDto.java
├── entity/
|──── UserEntity.java
├── mapper/
|──── UserMapper.java
├── repository/
|──── UserRepository.java
└── service/
|──── UserService.java
```

And there is a sample code in generated java files:

```java
// UserController.java

package com.example.project.user.controller;

public class UserController {
    // TODO: implement UserController
}
```


## **📁 Example Project Layout**

```
src/
└── main/
    └── java/
        └── com/
            └── example/
                └── project/
                    ├── user/
                    │   ├── controller/
                    │   ├── dto/
                    │   ├── entity/
                    │   ├── mapper/
                    │   ├── repository/
                    │   └── service/
                    └── product/
                        └── ...
```

## **🧩 Planned Features**

* Add annotations to stub classes.
* Add dto, mapper, or service separately with future commands (e.g. sputils makedto)
* Configuration via .sputilsrc file

## **🧑‍💻 License**

GPL-3.0 — You are free to use, modify, and distribute this project, provided that any derivative work is also licensed under the GPL-3.0.

## **🤝 Contributions**

Got ideas or improvements? Feel free to submit a pull request or open an issue. Let's make sputils a developer-friendly Spring CLI tool together!
