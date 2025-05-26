# **🛠️ sputils**

sputils is a lightweight command-line utility to scaffold feature-based package structures in a Spring Boot project.

It follows the **package-by-feature** design pattern — organizing code into cohesive feature modules, each containing its own controller, service, entity, repository, DTOs, and mappers.

## **📦 Features**

* Quickly scaffold a new feature module (like Django's startapp)
* Clean, organized folder structure inside your base package
* Easily extensible for future Spring-related CLI commands

## **🚀 Getting Started**

### **1. Clone or Copy the Script**

Download or copy the sputils Bash script and place it in your project root or somewhere in your $PATH.

Make it executable:
```bash
chmod +x sputils
```

Optionally move it globally:
```bash
sudo mv sputils /usr/local/bin/sputils
```

### **2. Configure Your Base Package**

In the script, set your Java base package and source path at the top:
```bash
# sputils 
BASE_PACKAGE="com.example.project"  # 🔁 Change to match your project package 
SRC_PATH="src/main/java"
```

## **⚙️ Usage**

```bash
sputils <command> [options]
```

### **Available Commands:**

#### `startapp <feature-name>`

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

Each folder includes a `.gitkeep` file to preserve directory structure.

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

* Generate stub classes (e.g., UserController.java, UserService.java, etc.)
* Support for test folder generation
* Add dto, mapper, or service separately with future commands (e.g. sputils makedto)
* Configuration via .sputilsrc file

## **🧑‍💻 License**

MIT — feel free to copy, modify, and use in any Spring Boot project.

## **🤝 Contributions**

Got ideas or improvements? Feel free to submit a pull request or open an issue. Let's make sputils a developer-friendly Spring CLI tool together!
