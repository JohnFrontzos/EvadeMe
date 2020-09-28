# EvadeMe
### A heuristics evasion library for Android
1. Add the maven repository to your project's allprojects closure in the gradle.build file
```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
2. Add the dependency to your app's build.gradle file
```groovy
dependencies {
    implementation 'com.github.evilthreads669966:evademe:-SNAPSHOT'
}
```
3. Use the evade ktx function inside of any android context.
```kotlin
evade {
    Log.d("EVADE", "EVIL THREADS");
}.onEscape{
    Toast.makeText(this, "We evaded with networking", Toast.LENGTH_LONG).show()
}.onSuccess {
    Toast.makeText(this, "We executed the paylod with networking", Toast.LENGTH_LONG).show()
}
```
Any code inside of the evade scoping function is safe from analysis. 
This allows you to develop malware or spyware that is not able to be tested by people.
