# GITHUB jenkins action parametrized

[![Travis][travis-image]][travis-url]
![License][license-image]
![Issues][issues-image]

## USAGE

### GitHub Actions

#### Inputs

##### `jenkins`

**Required** url  Parameter. Default `"https://toniflorithomar.cat"`.
**Required** user Parameter. Default `"test"`.
**Required** token Parameter. Default `"test"`.
**Required** job Parameter. Default `"/job/test"`.
**OPTIONAL** parameters Parameter. Default `"key1=value1&key2=value2&key3=value3"`. (Use & separator to Multiple key values)

#### Example usage

```bash
name: Trigger Jenkins
on: push
jobs:
  curl:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: jenkins
      uses: l3andro/jenkins-action-parametrized@master
      with:
        url: {{ URL }}
        user: {{ Jenkins User ID }}
        token: {{ Jenkins User Token ID }}
        job: {{ jenkins Job path }} `example /job/test`
        parameters: {{ jenkins parameters for parametrized jobs }}

```

