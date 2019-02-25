---
tags: [kotlin]
---

# Kotlin

* [Reference](https://kotlinlang.org/docs/reference/)
* [Kotlin Playground: Edit, Run, Share Kotlin Code Online](https://play.kotlinlang.org/)


## Learn

* [Tutorials](https://kotlinlang.org/docs/tutorials/)
* [Kotlin Koans: The Best Way To Learn Kotlin for Java Developers](https://play.kotlinlang.org/koans/overview)
* [Kotlin for Android Developers | Udacity](https://eu.udacity.com/course/kotlin-for-android-developers--ud888)
* [Build Your First Android App in Kotlin](https://codelabs.developers.google.com/codelabs/build-your-first-android-app-kotlin/index.html#0)

## Android

* [Kotlin for Android](https://kotlinlang.org/docs/reference/android-overview.html)
* [Kotlin and Android  |  Android Developers](https://developer.android.com/kotlin/)


* [Kotlin Android Extensions](https://kotlinlang.org/docs/tutorials/android-plugin.html)
* [Kotlin/anko: Pleasant Android application development](https://github.com/Kotlin/anko)
* [RecyclerView and Kotlin](https://medium.com/redso/trap-in-kotlin-android-extensions-d07be00759fa)




### Sample Apps
* [Samples apps](https://developer.android.com/samples/?language=kotlin)
* [Introducing Android Sunflower – Android Developers – Medium](https://medium.com/androiddevelopers/introducing-android-sunflower-e421b43fe0c2)


### Material Design

 

### RetroFit

* [Supercharging Retrofit with Kotlin – The Coinbase Blog](https://blog.coinbase.com/supercharging-retrofit-with-kotlin-f01096ad8aa7)

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

