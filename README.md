# Anagver
Android-Studio Auto versioning script

## What is this doing?
The Goal were to create a simple versioning for small projects.
So this scripts provide together a simple versioning that keeps the functionality of the Apply changes button in Android-Studio.
By running any build in Android-Studio the versions gets incemented but not included in the Manifest.xml
But on a git commit the versions are added together and included in the commit and the next build.
After commiting your changes youll have to use the Run action once because the now included versions are modifications to the Manifest.xml

Only Patch Build and Version numbers are increased ( build everytime and patch and version every assembly task ).
Minor and Major versions are excluded as they are not build-proccess defined.

## Reqirements to use this
These scripts are designed to work with android-studio (tested 3.5.2) and gradle (5.4.1)
if you have different versions, double check if the output matches your expectations.

## Installation
copy the the task `commitVersion` and the function `autoincrementVersion` from the `build.gradle` into your app/build.gradle or yourmodulehere/build.gradle

copy `versions.properties` into the same directory

copy the file `pre-commit` into your `.git/hooks/` or paste the line
`./gradlew commitVersion -Pcommit`
into the exsisting file

## Planned
- improve licensing
