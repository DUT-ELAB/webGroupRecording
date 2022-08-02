# Week 7 Web表单

这周我们学习下表单，之后打算留一周时间去巩固JavaScript，整体过一遍JavaScript的教程，了解ES6特性，在Web开发这块JavaScript讲的比较粗糙。接着学一下Ajax，主要用axios，jQuery目前不做打算，对Promise还不熟悉的同学需要注意了，之后打算学Bootstrap和React。现在这些只是初步打算，到时候根据情况决定吧。

## Introduction

本周将进行Web表单的学习，HTML 表单是用户和 web 站点或应用程序之间交互的主要内容之一。它们允许用户将数据发送到 web 站点。大多数情况下，数据被发送到 web 服务器，但是 web 页面也可以自己拦截它并使用它。

## Tasks

MDN上进行学习，[学习目录](https://developer.mozilla.org/zh-CN/docs/Learn/Forms)，注意，如果遇到图片无法加载的情况（例如[在创建我的第一个表单](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Your_first_form)中图片无法加载），把URL中的zh-CN替换为en-US即可正常访问。另外其中有两个网页为英文的，如果英语比较好可以直接看，当然对于Chrome直接右键翻译就行，翻译出来的文章也很容易读懂。

### 基本指南

- [你的第一个表单](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Your_first_form)

  本系列的第一篇文章提供了您第一次创建 HTML 表单的经验，包括设计一个简单表单、使用正确的 HTML 元素实现它、通过 CSS 添加一些非常简单的样式，以及如何将数据发送到服务器。

- [如何构造 HTML 表单](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/How_to_structure_a_web_form)

  有了基础知识，我们现在更详细地了解了用于为表单的不同部分提供结构和意义的元素。

### 不同的表单控件

- [原生表单控件](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Basic_native_form_controls)

  我们从详细了解原始 HTML `<input>` 元素的类型开始，同时学习在收集不同类型数据时可用的选择。

- [HTML5 input 的类型 (en-US)](https://developer.mozilla.org/en-US/docs/Learn/Forms/HTML5_input_types)

  在这里，我们深入挖掘 `<input>` 元素，了解 HTML5 发布时提供的其它 input 类型，以及它们提供的各种 UI 弓箭和数据收集增强功能。此外，我们可以了解 `<output>` 元素。

- [其它表单控件 (en-US)](https://developer.mozilla.org/en-US/docs/Learn/Forms/Other_form_controls)

  接下来，我们学习所有 非`<input>` 表单控件，以及相关的工具，如：`<select>`、`<textarea>`、`<meter>`、`<progress>`

### 表单样式指南

- [HTML 表单样式](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Styling_web_forms)

  本文介绍了使用 CSS 的样式表单，包括您可能需要了解的基本样式任务的所有基础知识。

- [高级表单样式](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Advanced_form_styling)

  在这里，我们将看到一些更高级的表单样式技术，这些技术需要在处理一些更难以设置样式的元素时使用。

- [UI 伪类 (en-US)](https://developer.mozilla.org/en-US/docs/Learn/Forms/UI_pseudo-classes)

  一个关于在 HTML 表单中使用 UI 伪类以根据表单状态自动设置样式。

### 验证和提交表单数据

- [表单数据验证](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Form_validation)

  发送数据还不够——我们还需要确保用户填写表单的数据格式是正确的以在后续流程中正确处理它，而且它不会破坏我们的应用程序。我们还希望帮助用户正确填写表单，让他们在使用应用程序时不会感到困扰。表单验证帮助我们实现这些目标，本文将告诉您需要了解的内容。

- [发送表单数据](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Sending_and_retrieving_form_data)

  本文讨论当用户提交一个表单时，会发生什么情况——表单数据的去向，以及当表单数据到达指定位置时我们如何处理？我们还研究了与发送表单数据相关的一些安全问题。

### 高级指南

以下文章对于学习路径来说没那么重要，但是当你掌握了上述技术并向了解更多内容时，它们会变得有趣且实用。

- [如何构建自定义表单控件](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/How_to_build_custom_form_controls)

  在某些情况下，原生表单部件无法提供您需要的东西，例如，由于样式或功能。在这种情况下，您可能需要使用原生 HTML 构建自己的表单小部件。本文将说明您是如何做到这一点的，以及在实际案例研究中需要注意的事项。

- [通过 JavaScript 发送表单](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Sending_forms_through_JavaScript)

  本文将讨论如何使用表单来构建 HTTP 请求，并通过定制的 JavaScript 发送它，而不是标准的表单提交。它还说明了为什么要这么做，以及这样做的意义。（请参阅[使用 FormData 对象](https://developer.mozilla.org/zh-CN/docs/Web/API/FormData/Using_FormData_Objects)。）

- [表单控件的 CSS 属性兼容性表](https://developer.mozilla.org/zh-CN/docs/Learn/Forms/Property_compatibility_table_for_form_controls)

  最后一篇文章提供了一个方便的参考，让您可以确定 CSS 属性与表单元素的兼容性关系。