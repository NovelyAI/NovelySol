# [Novely](https://novely.site)

Novel Engine for creating interactive stories

- **Multilanguage**: Enable users to access content in multiple languages and handle pluralization in a simple and intuitive way
- **TypeScript**: Development with efficiency, type checking, and smart auto complete
- **Modularity in Mind**: Opt-in features, instead of opting-out! Lightweight and highly customizable

## Community

This is our official [Twitter](https://x.com/NovelyOnSol) 

## Demo

You can see working demo [here](https://novely-demo.deno.dev/)

## Documentation and Getting Started

You can find documentation on our [Twitter](https://x.com/NovelyOnSol).

## Examples

```ts
import { createSolidRenderer } from '@novely/solid-renderer';
import { novely, EN } from '@novely/core';

const engine = novely({
  renderer: createSolidRenderer().renderer,
  translation: {
    en: {
      internal: EN
    }
  },
  characters: {
    Natsuki: {
      name: 'Natsuki',
      color: '#f388aa',
      emotions: {
        happy: './natsuki-happy.png'
      }
    }
  }
});

engine.script({
  start: [
    engine.action.showBackground('./school.png'),
    engine.action.showCharacter('Natsuki', 'happy'),
    engine.action.dialog('Natsuki', 'Whoa! I am very happy to see you!')
  ]
})
```

