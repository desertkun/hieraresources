# Hiera Resources
A helper module to automatically manage your hiera resources with [Hiera Editor](https://github.com/desertkun/hiera-editor).

It automatically defines resources from the `resources` property of your Hiera configurations:
```
classes:
  - <classes>
resources:
  <resource type XXX>:
    test:
      propertyA: 10
      propertyB: 12
    test2:
      propertyA: 20
```
The example above will automatically create two resources of type `XXX` with titles `test` and `test2` and give them appropriate properties.

## How to use it
Simply install the module, and add the `include hieraresources` as the only line in your `init.pp` file. It will automatically manage your classes and resources from Hiera.
