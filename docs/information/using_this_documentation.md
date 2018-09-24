# Using this Documentation

### Read Before Starting: 
> Please note that this is documenting closed-source code that has been decompiled.
> Various parts may be wrong or misunderstood by the person documenting them.

> Every class, struct, interface, enum, delegate, method, property, and field will each have its own page!

### Namespaces and Classes:

> Every namespace is seperated alphabetically from a-z on the sidebar. 
> Inside each namespace, every class is listed the same way.

### Class Layout and Structure
> To make everything easy, classes and structures have a very specific order that most similarly matches Microsoft's .NET documentation.

> Each class member will be layed-out in the following order:

> Functions:

> Name | Description
> - | -
> foo() | Returns bar

> Properties:

> Name | Description
> - | -
> foo | Gets bar

> Fields:

> Name | Description
> - | -
> foo | Gets or sets bar


### Function Layout and Structure

> All functions will be listed under alphabetical order.

> Function overloads will be listed on the same page under a different h1 header.

> Each function page will have the following order:

> Returns:

> Type | Description
> - | -
> object | The returned value

> Parameters:

> Type | Name | Description
> - | - | -
> object | foo | The parameter value

### Field/Property Layout and Structure

> All fields/properties will be listed under alphabetical order.

> If anything is readonly or doesn't have a setter, the description will start with 'Gets'. If it has a setter and is not readonly, the description will start with 'Getr or sets'.

> Each field and property page will have the following order:

> Returns:

> Type | Description
> - | -
> object | The returned value

### Enum Layout and Structure

> The values in enums will be listed in the ascending order of their integer values.

> If the compiler assigns the integer values, they will be arranged as so:

> Values:

> Value | Description
> - | -
> LEFT | The left side
> RIGHT | The right side

> If the integer values are manually set, they will be arranged as so:

> Values:

> Value | Integer | Description
> - | - |-
> LEFT | 2 | The left side
> RIGHT | 4 | The right side
