
### required directories ###

```
mkdir rpms srpms specs sources
```
To be used to test building RPMS on CentOS 7

## CentOS 5
### build in cwd with ###
```
docker build -t jackknifed/rpmbuild:cent5 cent5
```

### run with ###
```
docker run -i -t --rm jackknifed/rpmbuild:cent5 \
 -v $(pwd)/rpms/:/root/rpmbuild/RPMS \
 -v $(pwd)/srpms/:/root/rpmbuild/SRPMS \
 -v $(pwd)/specs/:/root/rpmbuild/SPECS \
 -v $(pwd)/sources/:/root/rpmbuild/SOURCES
```

## CentOS 6
### build in cwd with ###
```
docker build -t jackknifed/rpmbuild:cent6 cent6
```

### run with ###
```
docker run -i -t --rm jackknifed/rpmbuild:cent6 \
 -v $(pwd)/rpms/:/root/rpmbuild/RPMS \
 -v $(pwd)/srpms/:/root/rpmbuild/SRPMS \
 -v $(pwd)/rpmbuild/specs/:/root/rpmbuild/SPECS \
 -v $(pwd)/rpmbuild/sources/:/root/rpmbuild/SOURCES
```

## CentOS 7 ##
### build in cwd with ###
```
docker build -t jackknifed/rpmbuild:cent7 cent7
```

### run with ###
```
docker run -i -t --rm jackknifed/rpmbuild:cent7 \
 -v $(pwd)/rpmbuild/rpms/:/root/rpmbuild/RPMS \
 -v $(pwd)/rpmbuild/srpms/:/root/rpmbuild/SRPMS \
 -v $(pwd)/rpmbuild/specs/:/root/rpmbuild/SPECS \
 -v $(pwd)/rpmbuild/sources/:/root/rpmbuild/SOURCES
```
