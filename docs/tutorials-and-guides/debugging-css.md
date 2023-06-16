---
sidebar_position: 2
---

# Debugging CSS

## Sytmptoms and Strategies

Writing CSS can be a pain. Here are some common symptoms and strategies to help you debug your CSS.

### Symptom: Nothing is happening when I add or change CSS

### Strategy 1

Make sure you are using the correct selector. If you are using a class selector or id, make sure you have added the class to the element you want to style. Make a simple test. Add a border to the element. If the border shows up, then you know you are using the correct selector.

Add this to elements withtext

    .myClass {
        color: red;
    }

Add this to elements without text

    .myClass {
        border: 1px solid red;
    }

### Strategy 2

Make sure you are using the correct property. If you are using a property that is not supported by the element, nothing will happen. Make a simple test. Add a border to the element. If the border shows up, then you know you are using the correct property.
