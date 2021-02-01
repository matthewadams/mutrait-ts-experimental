# Strongly-Typed Traits in TypeScript

>NOTE: this is currently broken as we work to complete it.
>Collaboration is welcome, because this gets into some pretty challenging [advanced typings](https://www.typescriptlang.org/docs/handbook/advanced-types.html).

According to [the TypeScript doc on mixins](https://www.typescriptlang.org/docs/handbook/mixins.html), a mixin extends another class using the [subclass factory pattern](https://www.typescriptlang.org/docs/handbook/mixins.html#how-does-a-mixin-work).
This is not as reusable as it could be.
We'd like to support strongly-typed [traits](https://en.wikipedia.org/wiki/Trait_(computer_programming)) instead.

For the purposes of this discussion, traits are like mixins in reverse.
Instead of the mixin `extend`ing the class, the class `extend`s the trait.
This allows the author of the trait to provide default behavior that the class can override.
Instead of saying that "the class extends the trait", we prefer the phrase "the class expresses the trait". 

In languages like [Scala](https://docs.scala-lang.org/tour/traits.html), [Dart](https://dart.dev/guides/language/language-tour#adding-features-to-a-class-mixins) & others, traits are a first-class citizen.

The package [@northscaler/mutrait](https://www.npmjs.com/package/@northscaler/mutrait) has provided an implementation of traits in JavaScript for several years now.

This project is an attempt to describe traits in a manner compatible with TypeScript so that mutrait can be used in that environment as well.

## Prior Art

Ordering by most recent first, this is some of the prior art we're working with.

### chronograph
This project is inspired in part by [@northscaler/mutrait](https://www.npmjs.com/package/@northscaler/mutrait) and by part of [Bryntam's `chronograph` project](https://github.com/bryntum/chronograph), in particular, the mixin capabilities provided by the code [here](https://github.com/bryntum/chronograph/tree/master/src/class).
We are trying to collaborate with [the author](https://dev.to/chronograph/).

### typescript-trait-test

https://github.com/matthewadams/typescript-trait-test is a different attempt at this.
It is currently broken (as of this writing) & as-simple-as-possible-but-no-simpler attempt at traits in TypeScript by [the same author](http://matthewadams.me) as this repo.

### @northscaler/mutrait

The production-quality trait library for JavaScript (currently maintained & supported version).
This package is based on its predecessor, [mutrait](https://www.npmjs.com/package/mutrait) (last repo activity 2019-12 as of 2021-02).
This package is, in turn, based on _its_ predecessor, [mixwith](https://www.npmjs.com/package/mixwith) (last activity 2016-09 as of 2021-02).
