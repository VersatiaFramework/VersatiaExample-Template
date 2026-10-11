# VersatiaExample-Topic-Feature

One sentence: what this example shows.

Part of the [Versatia examples](https://github.com/VersatiaFramework/VersatiaExamples); documentation: [Page title](https://versatiaframework.github.io/VersatiaDocs/docs/page).

**Start with** [`Feature.kt`](src/main/kotlin/com/github/marcoral/versatia/example/topic/Feature.kt).

## What the log shows

```
[Feature] the lines the server logs when the plugin starts
```

## Things to try

- A change the reader can make and what happens then.

## Building

Requires JDK 21 and VersatiaStarter with what it exports (VersatiaAPI, the module APIs) in your
local Maven repository (`./gradlew publishToMavenLocal` in each checkout; see
[Building the framework](https://versatiaframework.github.io/VersatiaDocs/docs/contributing/building));
running it requires a Paper 1.21.4 server with VersatiaCore installed.

```bash
./gradlew build
```

To have the JAR copied to your server after every build, copy `local.properties.example` to
`local.properties` and set `pluginsDir`. The generated descriptor is in
`build/generated/ksp/main/kotlin`; open it to see exactly what the runtime executes.

## Using this template

1. Create the repository from this template, named `VersatiaExample-<Topic>-<Feature>`.
2. Rename `rootProject.name` in `settings.gradle.kts`, `name` and `main` in `plugin.yml`, the
   package and the main class.
3. Replace this README, keeping its sections.
4. Add the example to the [VersatiaExamples](https://github.com/VersatiaFramework/VersatiaExamples) catalogue and an
   example card to the documentation page it illustrates.
