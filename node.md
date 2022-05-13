**xxx**
```
```

**调试配置**
```
org.gradle.jvmargs=-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=5005
-Dorg.gradle.debug=true
```

**task**
```
task hello {
    doFirst {
        println "aaaaaaaaaaaaaaaaa"
    }

    doLast {
        println "bbbbbbbbbbbbbbbbb"
    }
}
```

**list循环**
```
def list = [1,2,3,4,5,6]
list.each {
        println it
}
```

**map**
```
def map = ["width":100,"height":200]
println map.getClass().name
println map["width"]
println map["height"]
map.each {
   println "key:${it.key} value:${it.value}"
}
```

