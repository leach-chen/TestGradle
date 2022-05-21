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

**for**
```
for(int i in 1..10)
{
   
}
```

**method**
```
def method1(a,b){
    if(a > b) {
        println a + b
    }else{
        println a - b
    }
}
method1(1,2)

def method2(closure)
{
   closure(1,2)
}
method2{a,b -> {
     println "${a},${b}"
  }
}
```
**task**
```
def Task myTask = task exTask
myTask.group = BasePlugin.BUILD_GROUP
myTask.description = "11111111111111111"
myTask.doLast {
    println"group:${group},description:${description}"
}
```


**task dependsOn**
```
task hello1 {
 println("hello1")
}

task hello2 {
 println("hello2")
}

task hello {
    dependsOn hello1,hello2
}
```


**project**
```
project.hasProperty("xxx") //检测是否有这个属性
```

**ext**
```
ext {
    name = "123"
    age = "123"
}
println "name is:${project.ext.name}"
```

**-P**
```
task myTask{
    println "${project.hasProperty("test")}"
}
./gradlew exTask -Ptest=123
```