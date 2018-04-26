Build:
```
docker build . --tag mans0954/sphinx
```
Run:
```
docker run -u $( id -u $USER ):$( id -g $USER )  -v $PWD:/sphinx --rm mans0954/sphinx SPHINXBUILD='python3 -msphinx' html latexpdf
```
Shortcut:
```
alias sb="docker run -u $( id -u $USER ):$( id -g $USER )  -v $PWD:/sphinx --rm mans0954/sphinx"
sb latexpdf html
```
Enter container:
```
docker run -v $PWD:/sphinx -ti --rm --entrypoint=bash mans0954/sphinx
```
