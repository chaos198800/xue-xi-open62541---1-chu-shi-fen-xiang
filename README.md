# 学习open62541 --- [1] 初始

本资源文件提供了关于open62541的初始学习内容，帮助初学者了解如何编译和运行open62541的简单示例。

## 内容概述

1. **下载源码**：介绍了如何从GitHub下载open62541的源码，并解释了如何下载子模块以启用特殊功能。
2. **官方文档**：提供了获取官方文档的方法，并建议下载后上传到云端以备查阅。
3. **编译**：详细说明了在Ubuntu 16.04环境下如何使用CMake进行编译，并解释了CMake命令行选项的作用。
4. **运行demo**：提供了两种运行demo的方法，分别介绍了如何使用静态库和单文件版本进行编译和运行。
5. **小结**：总结了本文的主要内容，并鼓励读者进一步阅读相关文档以深入学习。

## 使用说明

1. **下载源码**：
   - 使用以下命令下载open62541的源码：
     ```bash
     git clone -b v1.1.6 https://github.com/open62541/open62541.git
     ```
   - 下载子模块：
     ```bash
     git submodule update --init --recursive
     ```

2. **编译**：
   - 进入源码根目录，创建并进入build目录：
     ```bash
     mkdir build
     cd build
     ```
   - 使用CMake进行配置：
     ```bash
     cmake -DUA_ENABLE_AMALGAMATION=ON ..
     ```
   - 运行make生成文件：
     ```bash
     make
     ```

3. **运行demo**：
   - 方法一：使用静态库
     - 创建目录并拷贝libopen62541.a和open62541.h文件。
     - 创建server.c、client.c和CMakeLists.txt文件。
     - 运行CMake和make生成可执行文件。
   - 方法二：使用单文件版本
     - 创建目录并拷贝open62541.c和open62541.h文件。
     - 创建server.c、client.c和CMakeLists.txt文件。
     - 运行CMake和make生成可执行文件。

## 注意事项

- 在Ubuntu 18.04及以上版本中编译时，可能会遇到链接问题，建议检查CMake版本并进行相应调整。
- 建议使用Debian系统进行编译，以避免潜在问题。

## 贡献与反馈

如果您在使用过程中遇到任何问题或有改进建议，欢迎提交反馈或贡献代码。

---

通过本资源文件，您将能够初步掌握open62541的编译和运行方法，为进一步学习和应用打下基础。

## 下载链接

[学习open62541---1初始分享](https://pan.quark.cn/s/292291e7672b)