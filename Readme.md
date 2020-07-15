- Gradle Project is a collection of tasks.
- task is a collection of actions.
- Actions are functions performed by gradle in a acylic way.

- Gradle uses Project Object Model. so every sytnax in the build.gradle file extends `project` object. **example:** `repositories { mavencentral() }` can also declared as `project.repositories { mavencentral() }`

**Proerties in a gradle file**
- To list all the properties what can used in build.gradle file -> run terminal command `gradle properties`. or search in https://docs.gradle.org/current/dsl/org.gradle.api.Project.html

**Tasks**
- To view all available gradle tasks run `gradle tasks` command.

**List all projects in repo**
- `./gradlew projects`

**Dependencies**
- find dependecines and its dependencies `./gradlew dependencies` or `./gradlew dependencies --configuration compile` <- runs only the 

- Gradle project can have multiple child gradle projects. To find the gradle child projects look at setting.gradle file. with syntax `include ${new-project}` where `new-project` is a child gradlw project. this child project has it own build.gradle file.

- A gradle child project can used as a dependency in other gradle project.
````
Example: project-a has dependency on project-b

In project-a build.gradle

dependencies {
    compile project(':project-b') <- declared project-b as requiered at compile for project-a, and project-a build artifact will include project B aswell.
}
````
