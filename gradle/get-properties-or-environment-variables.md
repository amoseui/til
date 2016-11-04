# Get properties or environment variables

Get some variables from hidden files or environment

Set variables in gradle.properties
```ruby
KEY="AZ2Fdfjlafj23jfaZKEF"
```
or

export environment variables, usually save on CI server
```bash
export KEY="AZ2Fdfjlafj23jfaZKEF"
```
---

in build.gradle
```ruby
def key = project.hasProperty('KEY') ? KEY : "$System.env.KEY"

...

android {
  defaultConfig {
    ...
    buildConfigField 'String', 'KEY', "\"${key}\""
  }
}
```
---

Set constants from BuildConfig
```java
private static final String SECRET_KEY = BuildConfig.KEY;
```
