https://developer.android.com/training/dependency-injection/hilt-android#kts

gradle
```
plugins {
  ...
  id("com.google.dagger.hilt.android") version "2.56.2" apply false
}
```

app/gradle
```
plugins {
  id("com.google.devtools.ksp")
  id("com.google.dagger.hilt.android")
}

android {
  ...
}

dependencies {
  implementation("com.google.dagger:hilt-android:2.56.2")
  ksp("com.google.dagger:hilt-android-compiler:2.56.2")
}
```

```
Plugin [id: 'com.google.devtools.ksp'] was not found in any of the following sources:
```


gradle에 추가
```
id("com.google.devtools.ksp") version "2.0.21-1.0.27" apply false
```

# For Torang
```
root/gradle
id("com.google.dagger.hilt.android") version "2.46" apply false

app/gradle
id("kotlin-kapt")
id("dagger.hilt.android.plugin")

implementation("com.google.dagger:hilt-android:2.46")
kapt("com.google.dagger:hilt-android-compiler:2.46")
```