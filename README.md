# Nested Vue Accordion

Nested Vue Accordion is a lightweight and versatile Vue.js component that enables you to effortlessly create multilevel accordion interfaces. Whether you're building a navigation menu, a FAQ section, or any other content structure requiring nested collapsible panels, Nested Vue Accordion has got you covered.

## Features

- **Multilevel Nesting:** Easily nest accordion panels within each other to create complex hierarchical structures.
- **Flexible Configuration:** Customize the appearance and behavior of the accordion through simple props.
- **Lightweight and Performant:** Built with Vue.js, Nested Vue Accordion is lightweight and optimized for performance.

## Installation

You can install Nested Vue Accordion via npm:

```bash
npm install nested-vue-accordion

Usage
-----

### Basic Example

Here's a basic example demonstrating how to use Nested Vue Accordion:

<template>
  <nested-vue-accordion :items="accordionItems" />
</template>

<script>
import { NestedVueAccordion } from 'nested-vue-accordion';

export default {
  name: 'Parent-component',
  components: {
    NestedVueAccordion,
  },
  data() {
    return {
      accordionItems: [
        {
          title: "Category A",
          children: [
            {
              title: "Subcategory 1",
              children: [
                {
                  title: "Item 1",
                },
                {
                  title: "Item 2",
                },
              ],
            },
            {
              title: "Subcategory 2",
              children: [
                {
                  title: "Item 3",
                },
                {
                  title: "Item 4",
                },
              ],
            },
          ],
        },
        {
          title: "Category B",
          children: [
            {
              title: "Item 5",
            },
            {
              title: "Subcategory 3",
              children: [
                {
                  title: "Item 6",
                },
                {
                  title: "Item 7",
                },
              ],
            },
          ],
        },
      ],
    };
  },
};
</script>

### Advanced Example

Here's a more advanced example demonstrating nested accordion panels:

<template>
  <nested-vue-accordion :items="accordionItems" />
</template>

<script>
import { NestedVueAccordion } from 'nested-vue-accordion';

export default {
  name: 'AccordionExample',
  components: {
    NestedVueAccordion,
  },
  data() {
    return {
      accordionItems: [
        {
          title: "Category A",
          children: [
            {
              title: "Subcategory 1",
              children: [
                {
                  title: "Item 1",
                },
                {
                  title: "Item 2",
                },
              ],
            },
            {
              title: "Subcategory 2",
              children: [
                {
                  title: "Item 3",
                },
                {
                  title: "Item 4",
                },
              ],
            },
          ],
        },
        {
          title: "Category B",
          children: [
            {
              title: "Subcategory 3",
              children: [
                {
                  title: "Item 5",
                },
                {
                  title: "Item 6",
                },
              ],
            },
            {
              title: "Subcategory 4",
              children: [
                {
                  title: "Item 7",
                },
                {
                  title: "Item 8",
                },
              ],
            },
          ],
        },
      ],
    };
  },
};
</script>

## Documentation

For detailed documentation and customization options, please visit the [Nested Vue Accordion GitHub repository](https://github.com/hemant-rao/nested-vue-accordion).

## Contributing

Contributions are welcome! Please feel free to open an issue or submit a pull request.
```
