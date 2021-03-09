---
title: Monarch Framework Introduction

Id: amfconIntroductionMain
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 20

keywords: Monarch introduction, about
keywords: introduction to ASNA Monarch
keywords: ASNA Monarch, introduction
keywords: concepts, ASNA Monarch, introduction
keywords: ASNA Monarch, about
keywords: ASNA Monarch, display file support
keywords: Monarch introduction, execution context support
keywords: Monarch introduction, display file support
keywords: Monarch introduction, interactive application support
keywords: display files, support in Monarch Framework
keywords: execution context support, ASNA Monarch classes
keywords: execution context support, Job class
keywords: execution context support, Program class
keywords: execution context support, ClProgram class
keywords: display file support, ASNA Monarch classes
keywords: display file support, WebJob class
keywords: display file support, WebDisplayFile class
keywords: display file support, WebDevice class
keywords: display file support, Page class
keywords: display file support, web server controls
keywords: program execution management, program activation
keywords: program activation in Monarch Framework
keywords: program execution management, program invocation
keywords: program state in Monarch Framework
keywords: concepts, ASNA Monarch, ILE Model
keywords: concepts, ASNA Monarch, AVR support
keywords: display files, ASNA Monarch classes
keywords: display files, WebJob class
keywords: display files, WebDisplayFile class
keywords: display files, WebDevice class
keywords: display files, Page class
keywords: display files, web server controls

---

As part of the ASNA Monarch family of products, the Monarch Framework facilitates the migration of RPG applications. The Framework is comprised of a set of classes and a particular style of application creation. An application that follows this style and uses these classes is termed a Monarch Family Application.

The Monarch Framework borrows many of its concepts and terminology from the IBM i. Several of these concepts are made concrete via MonarchFX components and others are provided via methods or properties of these components. These components are divided into two groups. The first one deals with providing an **Execution Context** for the application, while the second provides **Display File** support for interactive applications.

#### Execution Context
These classes form the support for Execution Context:
<dl>
        <dd>
          [Job](amfJobClass.html)
        </dd>
        <dd>
          [Program](amfProgramClass.html)
        </dd>
        <dd>
          [CLProgram](amfCLProgramClass.html)
        </dd>
</dl>

#### Display File support for interactive applications
These classes and controls form the support for interactive applications:
<dl>
        <dd>
          [WebJob](amfWebJobClass.html)
        </dd>
        <dd>
          [
          WebDisplayFile](amfWebDisplayFileClass.html)
        </dd>
        <dd>
          [
          WebDevice](amfWebDeviceClass.html)
        </dd>
        <dd>
          [Page](amfPageClass.html)
        </dd>
        <dd>DDS like controls ([Web
        Server Controls](amfWebServerControlsOverview.html))</dd>
</dl>

#### Next: [ Execution Context](amfconExecutionContext.html)

#### See Also
[What's New](amfWhatsNewin72.html) <br /> [Reference Library](amfReferenceMain.html) 
