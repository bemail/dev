<h3 align="center">Take Action</h3>
<p align="center">This is an action to assign yourself to an issue for a repo you are not a contributor to.<p>

## Usage

This GitHub Action lets a prospective contributor assign themselves to an issue, and optionally leaves a comment on the issue.


## Setup

This GitHub Action requires a GITHUB_TOKEN and can be optionally configured with a message to the prospective contributor.
  
```yaml
# .github/workflows/take.yml 
name: Assign issue to contributor
on: 
  issue_comment:

jobs:
  assign:
    name: Take an issue
    runs-on: ubuntu-latest
    steps:
    - name: take the issue
      uses: bdougie/take-action@main
      env:
        GITHUB_TOKEN: ${{ github.token }}
      with:
        message: Thanks for taking this issue! Let us know if you have any questions!
```
