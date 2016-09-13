``` 
# make sure you GOPATH is set to the workspace root
# and $GOBIN=$GOPATH/bin
cd $GOPATH
mkdir -p src/github.com/openshift
git clone git@github.com:openshift/imagebuilder.git src/github.com/openshift/imagebuilder

# fix the Godeps/Godeps.json glog Ref
cd src/github.com/openshift/imagebuilder/
godep restore

cd $GOPATH
go install src/github.com/openshift/imagebuilder/cmd/imagebuilder/imagebuilder.go
```
