# composition-over-inheritance

## Difference between composition and inheritance in Kotlin, using a simple `MainActivity`.

Composition is in the file `MainActivityComposition`. We use the `by` keyword from Kotlin to implement it gracefully.
Inheritance is in the file `MainActivityInheritance`. We use the classical `BaseActivity` pattern.

Difference is clear: We'll have only one activity.

## Explaining the Kotlin Keyword

Just look at the signature of the `MainActivityComposition` class:

```kotlin
MainActivityComposition : MainActivity(), ViewStarter by ViewStarterImpl

The problem can be probably understood as `ViewStarter by ViewStarterImpl`, but we can just understand it as the following: 
"I'm `MainActivityComposition`, and I will implement the `ViewStarter` interface, but I will not implement it myself. 
I will delegate this to the `ViewStarterImpl` object to do it for me!"



