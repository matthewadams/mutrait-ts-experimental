# Strongly-Typed Traits in TypeScript

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
