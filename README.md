Avro schemas for project chaos:  
https://github.com/stodolkiewicz/project-chaos-backend

project chaos backend uses jitpack.

jitpack builds a jar based on a git tag.
> git tag v1.0.0  
> git push origin v1.0.0

Then, jitpack publishes it in its own repository.  
 >   version: same version as the tag.  
 >   groupId: com.github.[your-github-username]  
 >   artifactId: [github-repository-name]  

### To use the built jar as a dependency in another repository:
1. add jitpack repo
```xml
<project>
 ...
	<repositories>
        <repository>
            <id>jitpack.io</id>
            <url>https://jitpack.io</url>
        </repository>
    </repositories>
 ...
</project>
```

2. add your built dependency
```xml
<project>
 ...
    <dependencies>
        ...
        <dependency>
           <groupId>com.github.stodolkiewicz</groupId>
           <artifactId>project-chaos-avro-schemas</artifactId>
           <version>2.0.0</version>
       </dependency>
    </dependencies>
...
</project>
```
