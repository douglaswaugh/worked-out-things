# Working out how to run tests in VS Code

1. Add the necessary dependencies in project.json
```
{
    "dependencies": {
        "NUnit": "3.4.1",
        "dotnet-test-nunit": "3.4.0-beta-2"
    }
}
```

2. Set the testRunner in project.json
```
{
    "testRunner": "nunit"
}
```

3. Set buildOptions emitEntryPoint in project.json (or emit, it's false by default)
```
{
    "buildOptions": {
        "emitEntryPoint": false
    }
}
```

4. Restore the dependencies
```
dotnet restore
```

5. Run the tests
```
dotnet test
```