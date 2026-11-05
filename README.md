# VersatiaExample-Topic-Feature

One sentence: what this example shows.

Part of the [Versatia examples](https://github.com/VersatiaFramework/VersatiaExamples); documentation: [Example plugins](https://versatia.dev/docs/examples).

**Start with** [`ExamplePlugin.kt`](src/main/kotlin/dev/versatia/example/template/ExamplePlugin.kt).

## What the log shows

```
[Feature] the lines the server logs when the plugin starts
```

## Things to try

- A change the reader can make and what happens then.

## Building

Requires JDK 25 and VersatiaAPI and
VersatiaCatalog, which supplies every version, in your local Maven repository (`./gradlew publishToMavenLocal` in each checkout; see
[Building the framework](https://versatia.dev/docs/contributing/building));
running it requires a Paper 26.3 server with VersatiaCore installed. If "Things to try" reloads,
add: and the [CommandAPI](https://commandapi.jorel.dev) 12.x plugin for `/versatia reload`.

```bash
./gradlew build
```

To have the JAR copied to your server after every build, copy `local.properties.example` to
`local.properties` and set `pluginsDir`. The generated descriptor is in
`build/generated/ksp/main/kotlin`; open it to see exactly what the runtime executes.

The Versatia version is `versatiaVersion` in `gradle.properties`; `settings.gradle.kts` imports
the matching [VersatiaCatalog](https://versatia.dev/docs/getting-started/installation#versatia-catalog),
so the build script writes `libs.versatia.api` and `alias(libs.plugins.ksp)` instead of version
numbers.

## Using this template

1. Create the repository from this template, named `VersatiaExample-<Topic>-<Feature>`.
2. Rename `rootProject.name` in `settings.gradle.kts`, `name` and `main` in `plugin.yml`, the
   package and the main class.
3. Replace this README, keeping every section except this one; a two-plugin example adds a
   `Layout` section (see VersatiaExample-DI-SharedBeans). The build checks that `plugin.yml` parses
   and lists VersatiaCore under `depend:`.
4. Set the repository description to the README's first sentence.
5. Add the example to the [VersatiaExamples](https://github.com/VersatiaFramework/VersatiaExamples) catalogue and an
   example card to the documentation page it illustrates.
