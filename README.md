# package-rename-issue
 
 This project highlights an issue with gradle where on Windows if you rename a package where the only change is the case of the characters, gradle will not recognize that the generated classes should be put into a different package.
 
# Steps to Replicate

- Checkout the master branch
- Run a `./gradlew test`
- Checkout the uppercase branch (changed package to uppercase and renamed directories accordingly)
- Run a `./gradlew test`

The test will fail in the second test due to class not found errors.