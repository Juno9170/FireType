<script module>
  import { defineMeta } from '@storybook/addon-svelte-csf';
  import StoryBookComponent from './StoryBookComponent.svelte';

  // More on how to set up stories at: https://storybook.js.org/docs/writing-stories
  const { Story } = defineMeta({
    title: 'Example/Header',
    component: StoryBookComponent,
    // This component will have an automatically generated Autodocs entry: https://storybook.js.org/docs/writing-docs/autodocs
    tags: ['autodocs'],
    parameters: {
      // More on how to position stories at: https://storybook.js.org/docs/configure/story-layout
      layout: 'fullscreen',
    },
    args: {
        prop1: "Hello",
        prop2: "World",
    }
  });
</script>

<Story name="Logged In" args={{logged: true}}/>

<Story name="Logged Out" args={{logged: false}}/>