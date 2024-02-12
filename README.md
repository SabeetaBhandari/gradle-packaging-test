# gradle-packaging-test
Demo project to compare gradle packaging at springboot 3 and springboot 2, **when bootJar is disabled**

Change the spring boot version in build.gradle file to '2.4.8' -> The artifact generated is 'gradle-packaging-test-0.0.1-SNAPSHOT.jar'
Change the spring boot version in build.gradle file to '3.1.8' -> The artifact generated is 'gradle-packaging-test-0.0.1-SNAPSHOT-plain.jar'

Notice the '-plain' classifier in artifact name after the upgrade. 

It seems when bootJar is disabled, the generated jar doesn't have -plain in the artifact name in spring boot 2.4.8.
But when I upgrade springboot to '3.1.8', the artifact name is changed.

I know we can solve this by adding **classifier= ''** under jar task. But this extra step was not needed in spring boot 2.4.8 version.
I couldn't find any documentation related to it, exactly which version has this change. 


