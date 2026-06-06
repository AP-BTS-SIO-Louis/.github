# .github

````
name: "🛡️ Security check"

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  scan:
    uses: loutik/.github/.github/workflows/security.yml@main
````