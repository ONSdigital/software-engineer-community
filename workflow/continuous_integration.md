# Continuous Integration

#### Before raising a Pull Request
It is important to remember how code changes could affect continuous integration (CI). 

Any CI changes should be made as early as possible, ideally before raising a pull request. Examples of CI changes that could be made independently before merging any code changes are: 
* Adding/Removing/Changing environmental variables
* Build scripts added/removed
* Changing the build tools 
* A service is added/removed
* A github repository is renamed
* A service depends on a new Cloudfoundry service
* A change to how the tests run


#### After merging a Pull Request
Close attention should be made to CI. Any failure from the build of a service or test should be investigated and resolved immediately.