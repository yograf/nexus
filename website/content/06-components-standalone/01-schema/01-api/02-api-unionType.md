---
title: unionType
---

## unionType

[GraphQL Docs for Union Types](https://graphql.org/learn/schema/#union-types)

Union types are very similar to interfaces, but they don't get to specify any common fields between the types.

```ts
const MediaType = unionType({
  name: 'MediaType',
  description: 'Any container type that can be rendered into the feed',
  definition(t) {
    t.members('Post', 'Image', 'Card')
    t.resolveType((item) => item.name)
  },
})
```

Check the type-definitions or [the examples](https://github.com/graphql-nexus/schema/tree/develop/examples) for a full illustration of the various options for `unionType`, or feel free to open a PR on the docs to help document!
