# Marva Layout

Marva is organized into panels that each have a different purpose. They are:

1) Properties Panel
2) Edit Panel
3) Preview Panels
4) Linked Data Panel

All can be hidden from view except for the Edit Panel. This can be down under `View` in the Nav bar.

## Properties Panel

This panel has 2 sections: Navigation on top and the component library below that. This will cover the first part. For details on using the component library see [documentation here](../marva-tools/component-library.md).
The navigation section can jump you to a component, reorder things, and presents some extra information about the contents of a component.

### Navigation
This section is intended to help navigate the record quickly. It lists the Work, Instances, and any Items related that are part of the resource.

![Work and Instance group for resource](../images/image-1795008381493.png)

Each element in the list is a group that can be expanded by clicking on it. Doing so will show all of the components in that element.

![Expand Work element with components listed out](../images/image-1795008509070.png)

Clicking on any element will cause Marva to jump to that component.

![Navigate to a subject by clicking](../images/properties_navigation_click-1795008817300.webp)

### Reordering
The components in this panel can be dragged to change the order of them. Changes done in this way will only remain for the current session.

![Drag "Creator of Work" to the top of the Work](../images/move_creator_of_work.webp)

If you want the order to persist between records, you will need to use the buttons below the list of properties.

![Reorder Buttons](../images/image-1795009576933.png)

From left to right they are:

- Save the current order
- Load the saved order
- Load the default order (this will not remove your saved order)

In the Properties Panel, some components are underlined. These are the elements that need to be moved to set and save the order. If there are multiple subjects and you want to change where subjects appear, you will need to move the underlined subject heading. Clicking "save order" will cause the related components to move to the underlined component.

![Moving subject headings to top of work and saving order](../images/moving-and-saving-subject-pos.webp)

### Extra Info

To the left of the component names, there is an icon. It can be a dot, circle, or circle with a check. These icons tell you about what information is in the component.

- Dot = a component without any information
![Dot for an empty Title component](../images/image-1795010556997.png)
- Circle = component has data from the loaded record
![Circle representing Title loaded from record](../images/image-1795010473024.png)
- Circle with check = component has user added/edited data
![Circle with check for Title with user data](../images/image-1795010524978.png)

---

## Edit Panel

This is where cataloging work is done. It provides components based on the profile loaded. See [Create and Edit Descriptions](../create-and-edit-descriptions/index.md) for details. There are a lot of preferences that can change how this section appears and functions. The [Preference Reference](../Configuration/preferences-reference.md) has a break down of these.

---

## Preview Panels

Preview Panels provide several different options for view the data entered in the Edit Panel. There are 3 preview available.

1) OPAC - a text based view of the data
2) MARC - MARC and MARCXML views of the data (can be popped out into its own window)
3) XML - BF structured in XML

They can all be turned on, or all turned off. There are preferences that can change how these look and function.

---

## Linked Data Panel

This panel can help find and add information for a resource from 3rd party sources.

![Linked Data Panel](../images/image-1795011223894.png)

The panel is made of a few sections. There's a series of dropdowns on top with various information. The initial source of information is WorldCat. 

The bottom are various additional sources that are available to search for information.

Searching is based on the ISBN and if there are multiple ISBNs for the resource they can be switch between.

### Add information to a resource

Clicking a dropdown will expand it and show the information available from a source.

![Expanded 'Subject Heading' dropdown](../images/image-1795011651302.png)

If any of the values look like ones you'd like to add to the resource, click the "Add" button and it will appear in the correct component.

![Add 'Subject Heading' to resource](../images/add_subject.webp)
