# Kotlin Android Guide (WIP)

This repository will cover some topics that were hard for me initially during android development. I have learned many new things at my most recent internship and would like to share/document some of that here in this repository.

## Dependency Injection with Dagger Hilt
Dependency injection is a crucial part of building scalable apps, when building applications it is important to think about memory usage. When we want to access for example a database of some sort, we don't want to create multiple instances of local databases with hundreds of tables. This will knaw away at the System Heap as we continue to create new objections. Similarly, we would not want to instantiate many clients for the same network request it simply does not make sense. 

Dependency injection happens during compile time and after wards we can use this single instances anywhere in the app more efficiently that if we did the latter option. Please see the guide [here](https://github.com/JSDWRLD/Kotlin-Android-Guide/blob/main/DaggerHilt.md).

## Jetpack Compose

## Coroutines and Concurrency

## Room DB

## State Management
