Define the name to be used for the imagestream and buildconfig - each 
respective resource will have the abbreviation appended to it - example:
custom-bc /custom-is

The imagestream sourceImage is the image that you desire for the base
image while building your image. We use the cli image bc it allows
us to build everything in-cluster. The latest tag is for the imageStream
that gets provisioned - and latest is the default. 

The buildconfig points to the git repository where the source code is 
or containerfiles to be built are located. The .buildconfig.git.uri is the 
direct URL to the repository, and .buildconfig.git.contextDir is where the 
buildConfig should change into when running the build. 
.buildconfig.dockerfilePath is the location of the {Container,Docker}file to
be consumed. 

|Parameter|Explanation/Default Value|
|---------|-------------------------|
|name|`provide name for imagestream & buildconfig |
|sourceImage|`image-registry.openshift-image-registry.svc:5000/openshift/cli`|
|tag|`latest`|
|git.uri|`provide url for github repository`|
|git.ref|`main`|
|git.contextDir|`directory for build to switch into`|
|dockerfilePath|`ContainerFile`|
