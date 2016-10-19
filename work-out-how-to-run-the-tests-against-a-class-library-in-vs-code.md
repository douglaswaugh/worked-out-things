# Work out how to run the tests against a class library in VS Code

1. Create a global.json file in the root folder
```
{
  "projects": [
    "src",
    "test"
  ]
}
```

2. Create an class library project and test project in the project folders.

The test project folder must have a different name to the class library project, otherwise .Net Core sees it as a circular dependencey.

```
/roman-numerals
|__global.json
|__/src
   |__/roman-numerals
|__/test
   |__/test-roman-numerals
```

3. Add a reference to the class library project from the test project

```
{
  "dependencies": {
    "roman-numerals": {
      "target": "project"
    }
  }
}
```

4. Restore and build the class library project
```
dotnet restore src/roman-numerals
dotnet build src/roman-numerals
```

5. Restore and build the test project
```
dotnet restore test/test-roman-numerals
dotnet build test/test-roman-numerals
```

6. Red, green, refactor

7. Run the tests
```
dotnet test test/test-roman-numerals
```