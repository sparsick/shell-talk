# Demo Runbook

## httpie

```shell
http GET https://swapi.tech/api/starships
http GET https://swapi.tech/api/starships/9 --output starship-demo.json
```

## jq

```shell
cat starships.json| jq '.'
cat starships.json| jq '.results'
cat starships.json| jq '.results.[0]'
cat starships.json| jq '.results.[0].name'
cat starships.json| jq '.results.[].name'
```

## yq

```shell
cat starships.yaml | yq .
cat starships.yaml | yq . -y
cat starships.yaml | yq .results -y
cat starships.yaml | yq .results.[0] -y
cat starships.yaml | yq .results.[0].name -y
cat starships.yaml | yq .results.[].name -y

```

## sort
```shell
cat people.json | jq '.results.[].gender' | sort
```


## uniq

```shell
cat people.json | jq '.results.[].gender' | sort | uniq
cat people.json | jq '.results.[].gender' | sort | uniq -c
```


## dive

```shell
dive sparsick/spring-boot-demo
```


## trivy

```shell
trivy image sparsick/spring-boot-demo
trivy image --ignore-unfixed sparsick/spring-boot-demo
trivy image --ignore-unfixed sparsick/spring-boot-demo --format json
```
