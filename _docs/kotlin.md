---
tags: [kotlin]
---

# Kotlin

* [Reference](https://kotlinlang.org/docs/reference/)
* [Kotlin Playground: Edit, Run, Share Kotlin Code Online](https://play.kotlinlang.org/)


## Learn

* [Tutorials](https://kotlinlang.org/docs/tutorials/)
* [Kotlin Koans: The Best Way To Learn Kotlin for Java Developers](https://play.kotlinlang.org/koans/overview)

## Android

* [Kotlin for Android](https://kotlinlang.org/docs/reference/android-overview.html)
* [Kotlin Android Extensions](https://kotlinlang.org/docs/tutorials/android-plugin.html)
* [Kotlin/anko: Pleasant Android application development](https://github.com/Kotlin/anko)

### Dagger

* [Android Frameworks Using Annotation Processing](https://kotlinlang.org/docs/tutorials/android-frameworks.html#dagger)
* [kotlin-examples/gradle/kotlin-dagger at master · JetBrains/kotlin-examples](https://github.com/JetBrains/kotlin-examples/tree/master/gradle/kotlin-dagger)

### Kotlin Android Extensions

build.gradle
```
apply plugin: 'kotlin-android-extensions'
```

#### Parcelable 

````
import kotlinx.android.parcel.Parcelize

@Parcelize
class User(val firstName: String, val lastName: String, val age: Int): Parcelable
``` 

