# base-unit-trait-coast-bound

The `CoastBound` unit trait: a unit type with it is safe only near the coast.

A unit type with this trait may be lost if it ends its turn away from the coast.

For example: Civ1: Trireme. Civ2: flag 5 (Trireme).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(CoastBound)`:

```ts
import CoastBound from '@civ-clone/base-unit-trait-coast-bound/CoastBound';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, CoastBound));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
