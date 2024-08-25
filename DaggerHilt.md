# Guide to Dependency Injection

We will cover how to use Google Dagger hilt. First you must add the dependencies to your lib.versions.toml:

```
[versions]
hilt = "2.46"

[libraries]
google-dagger-hilt = { group = "com.google.dagger", name = "hilt-android", version.ref = "hilt" }
google-dagger-hilt-compiler = { group = "com.google.dagger", name = "hilt-android-compiler", version.ref = "hilt" }

[plugins]
google-dagger-hilt = { id = "com.google.dagger.hilt.android", version.ref = "hilt" }
```

Secondly we now must add into a project level gradle
```
plugins {
    alias(libs.plugins.google.dagger.hilt) apply false
}
```
and our module level gradle, do not worry about the error, it will get fixed during gradle build
```
plugins {
    kotlin("kapt")
    alias(libs.plugins.google.dagger.hilt)
}

dependencies {
    implementation(libs.google.dagger.hilt)
    kapt(libs.google.dagger.hilt.compiler)
}

kapt {
    correctErrorTypes = true
}
```
