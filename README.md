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
import NestedVueAccordion from 'nested-vue-accordion';

export default {
  name: 'Parent-component',
  components: {
    NestedVueAccordion,
  },
  data() {
    return {
      accordionItems: [
        {
          title: 'Panel 1',
          children: [
            { title: 'Subpanel 1' },
            { title: 'Subpanel 2' },
          ],
        },
        {
          title: 'Panel 2',
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
import NestedVueAccordion from 'nested-vue-accordion';

export default {
  name: 'AccordionExample',
  components: {
    NestedVueAccordion,
  },
  data() {
    return {
      accordionItems: [
        {
          title: 'Section 1',
          children: [
            { title: 'Subsection 1.1' },
            { title: 'Subsection 1.2' },
          ],
        },
        {
          title: 'Section 2',
          children: [
            {
              title: 'Subsection 2.1',
              children: [
                { title: 'Sub-subsection 2.1.1' },
                { title: 'Sub-subsection 2.1.2' },
              ],
            },
            { title: 'Subsection 2.2' },
          ],
        },
      ],
    };
  },
};
</script>

## Documentation

For detailed documentation and customization options, please visit the [Nested Vue Accordion GitHub repository](# Nested Vue Accordion

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
import NestedVueAccordion from 'nested-vue-accordion';

export default {
  name: 'Parent-component',
  components: {
    NestedVueAccordion,
  },
  data() {
    return {
      accordionItems: [
        {
          title: 'Panel 1',
          children: [
            { title: 'Subpanel 1' },
            { title: 'Subpanel 2' },
          ],
        },
        {
          title: 'Panel 2',
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
import NestedVueAccordion from 'nested-vue-accordion';

export default {
  name: 'AccordionExample',
  components: {
    NestedVueAccordion,
  },
  data() {
    return {
      accordionItems: [
        {
          title: 'Section 1',
          children: [
            { title: 'Subsection 1.1' },
            { title: 'Subsection 1.2' },
          ],
        },
        {
          title: 'Section 2',
          children: [
            {
              title: 'Subsection 2.1',
              children: [
                { title: 'Sub-subsection 2.1.1' },
                { title: 'Sub-subsection 2.1.2' },
              ],
            },
            { title: 'Subsection 2.2' },
          ],
        },
      ],
    };
  },
};
</script>

## Documentation

For detailed documentation and customization options, please visit the [Nested Vue Accordion GitHub repository](https://github.com/hemant-rao/nested-vue-accordion/).

## Contributing

Contributions are welcome! Please feel free to open an issue or submit a pull request.