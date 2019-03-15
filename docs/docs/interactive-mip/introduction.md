# 可交互式设计概述

## 概述

MIP 提供了为数众多的官方组件来满足开发者的需求。这些组件一般都封装或者实现了一些特定的样式或者功能，开发者一般只需要通过堆砌 MIP 组件，修改它们的样式，配置好相应的属性，就可以获得相应的 MIP 页面。在一些复杂的可交互 MIP 页面中，只通过配置组件属性是达不到设计要求的。

举个简单的例子，页面上点击某个按钮，然后弹出对话框。在这个例子里，涉及到了以下过程：

1. 按钮点击事件监听；
2. 按钮与对话框通信；
3. 对话框显示；

因此，MIP 需要提供一套机制来覆盖上述过程。MIP 组件在设计上遵循相互独立的原则，是某个功能或者样式的封装，通过对外暴露属性、事件和行为的方式来实现外部对组件的配置和使用。因此，在监听到组件抛出的事件时，动态地去触发别的组件的行为，或者是修改别的组件的属性，就可以实现组件之间的通信和交互。

在本章节中，我们将学习到事件监听与行为触发的 “on” 语法规则与使用，以及基于“数据驱动”的数据绑定语法 “m-bind”，并会学习到自定义 JS 的书写规范。通过本章节所学习到的内容，我们将可以更有机地把 MIP 组件串联起来，增强 MIP 页面的可交互性。

## 章节索引

- [事件监听与行为触发](./event-and-action.md)：介绍 “on” 语法规则与使用
- 数据绑定：介绍数据驱动的流程与用法
    - [数据定义](./data-binding/data-definition.md)：延伸介绍多种数据类型的定义方法
    - [数据获取、修改与观察](./data-binding/data-operation.md)：介绍数据获取、修改与观察的方法
    - [数据绑定语法说明](./data-binding/mip-bind.md)：介绍数据绑定语法 m-bind 和 m-text
    - [class 与 style 属性绑定语法说明](./data-binding/class-and-style-binding.md)：介绍绑定 class 和 style 属性的语法
- [自定义 JS](./custom-js-by-using-mip-script.md)：介绍 mip-script 的使用方法以及自定义 JS 的书写原则和规范