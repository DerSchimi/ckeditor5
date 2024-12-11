---
category: features
menu-title: List properties
meta-title: List properties | CKEditor 5 Documentation
meta-description: Learn how to configure and use the list properties feature in CKEditor 5, including custom list types.
---

# List properties

The list properties feature in CKEditor 5 allows you to control various aspects of lists, such as the marker, start index, and order. This feature is highly configurable and can be customized to fit your needs.

## Configuration

To configure the list properties feature, you need to add the `ListProperties` plugin to your editor and provide the desired configuration options. Here is an example configuration:

```javascript
import ListProperties from '@ckeditor/ckeditor5-list/src/listproperties';

ClassicEditor
    .create( document.querySelector( '#editor' ), {
        plugins: [ ListProperties, ... ],
        toolbar: [ 'bulletedList', 'numberedList', ... ],
        list: {
            properties: {
                styles: true,
                startIndex: true,
                reversed: true,
                customListTypes: [
                    {
                        commandName: 'customListType1',
                        label: 'Custom List Type 1',
                        icon: '<svg>...</svg>',
                        styles: [ 'customStyle1', 'customStyle2' ]
                    }
                ]
            }
        }
    } )
    .catch( error => {
        console.error( error );
    } );
```

### Custom List Types

The `customListTypes` configuration option allows you to define custom list types with their own styles. Each custom list type should have the following properties:

- `commandName`: The name of the command associated with the custom list type.
- `label`: The label for the custom list type.
- `icon`: The SVG icon for the custom list type.
- `styles`: An array of styles for the custom list type.

Here is an example of how to define a custom list type:

```javascript
customListTypes: [
    {
        commandName: 'customListType1',
        label: 'Custom List Type 1',
        icon: '<svg>...</svg>',
        styles: [ 'customStyle1', 'customStyle2' ]
    }
]
```

## Usage

Once the list properties feature is configured, you can use the toolbar buttons to control the list properties. The toolbar buttons for bulleted and numbered lists will be extended to include options for changing the list style, start index, and order.

### Bulleted List

The bulleted list button will include options for changing the list style to disc, circle, or square.

### Numbered List

The numbered list button will include options for changing the list style to decimal, decimal with leading zero, lower-roman, upper-roman, lower-latin, or upper-latin. It will also include options for setting the start index and reversing the list order.

### Custom List Types

If you have defined custom list types, their buttons will be added to the toolbar, allowing you to apply the custom styles to your lists.

## Examples

Here are some examples of how to use the list properties feature:

### Example 1: Changing the List Style

```javascript
editor.execute( 'listStyle', { type: 'circle' } );
```

### Example 2: Setting the Start Index

```javascript
editor.execute( 'listStart', { startIndex: 5 } );
```

### Example 3: Reversing the List Order

```javascript
editor.execute( 'listReversed', { reversed: true } );
```

### Example 4: Applying a Custom List Style

```javascript
editor.execute( 'customListType1', { type: 'customStyle1' } );
```

## Conclusion

The list properties feature in CKEditor 5 provides a powerful and flexible way to control the appearance and behavior of lists in your content. By configuring the available options and using the provided commands, you can create lists that meet your specific requirements.
