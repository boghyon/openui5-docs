<!-- loio36a5b130076e4b4aac2c27eebf324909 -->

| loio |
| -----|
| 36a5b130076e4b4aac2c27eebf324909 |

<div id="loio">

view on: [demo kit nightly build](https://openui5nightly.hana.ondemand.com/#/topic/36a5b130076e4b4aac2c27eebf324909) | [demo kit latest release](https://openui5.hana.ondemand.com/#/topic/36a5b130076e4b4aac2c27eebf324909)</div>

## Reusing UI Parts: Fragments

Fragments are light-weight UI parts \(UI sub-trees\) which can be reused, defined similar to views, but do not have any controller or other behavior code involved.

UI parts which are to be used in several views cannot be easily defined. They either have to be created as new controls, or they have to be created as views. Creating them as new controls results in a development overhead, while creating them as separate views results in a runtime overhead. In the latter case they would have a separate controller instead of having the same controller as the view does. Also, views and popup controls like dialogs do not go well together. The dialog content can be defined as a view but the dialog control itself always has to be written in the program.

To solve these issues, fragments have been introduced. They can be reused and, if source code is required and for event handler methods, they can connect to existing controllers of the "owning" view. This means that one important characteristic of fragments is that they are independent of the model-view-controller \(MVC\) concept and can be used without using MVC. However, if fragments are used together with views and controllers, fragments can make use of them and integrate them neatly.

Similar to `DocumentFragments` in HTML, the fragment itself has no HTML representation when it is inserted into the UI tree. Instead, its content is inserted. This means that fragments are not like controls, but more like a factory creating the contained controls. They support reuse and view modularization without adding overhead.

OpenUI5 provides different types of fragments:

-   XML fragments
-   HTML fragments
-   JS fragments

More fragment types can be implemented and plugged in.

Defining a fragment is similar to defining views within a separate file. The fragments simply end with `*.fragment` instead of `*.view`. Also, the same rules for file location apply.

**Related information**  


[Model View Controller \(MVC\)](Model_View_Controller_(MVC)_91f2334.md)

[Walkthrough Step 16: Dialogs and Fragments](Step_16_Dialogs_and_Fragments_4da7298.md)

