# composition-over-inheritance

## Difference between composition and inheritance in Kotlin, using a simple android sample with MainActivity.

Composition is in the file `MainActivityComposition`. We use the `by` keyword from Kotlin to implement it gracefully.

Inheritance is in the file `MainActivityInheritance`. We use the classical `BaseActivity` pattern.

Difference is clear: When using composition, we'll have only one activity, and the signature for ViewStarter is more intuitive than BaseActivity. BaseActivity tells nothing for us.

## Explaining the Kotlin `by` Keyword

Just look at the signature of the `MainActivityComposition` class:

```
MainActivityComposition : MainActivity(), ViewStarter by ViewStarterImpl
```

The problem can be probably understood what the hell is `ViewStarter by ViewStarterImpl`, but we can think about it as the following: 

"I'm `MainActivityComposition`, and I'll implement the `ViewStarter` interface, but I will not implement it myself. 
I will delegate this to the `ViewStarterImpl` object to do it for me!"

By doing this, `MainActivityComposition` can access all methods from the `ViewStarter`, without concern about implementation (It delegates to the ViewStarterImpl, remember?) 



