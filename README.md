Fork from the main repo to add docker-compose just for a basic setting for demo/test GoCD

If you don't have docker already, install from
https://docs.docker.com/docker-for-mac/


```
git clone https://github.com/valtaz/gocd-docker.git
cd gocd-docker
docker-compose build
docker-compose up
```

You can access the Go site via http://localhost:8153/go/pipelines

----------------------------------------------------------------------


This is the repository which contains the Dockerfiles and supporting scripts for:

https://registry.hub.docker.com/u/gocd/gocd-dev/

https://registry.hub.docker.com/u/gocd/gocd-agent/

https://registry.hub.docker.com/u/gocd/gocd-server/

https://registry.hub.docker.com/u/gocd/gocd-build-installer/

Follow those URLs for more details about the actual images. For instructions to build the Docker images yourself, check
the first line of each Dockerfile.

## Version control system clients

To keep image size minimal the GoCD server image only contains the Git client. To add other clients create your own image using this as a base.

e.x. to add Subversion:
```
FROM gocd/gocd-server:<version>
RUN apk --no-cache add subversion
```


## Contributing

We encourage you to contribute to Go. For information on contributing to this project, please see our [contributor's guide](http://www.go.cd/contribute).
A lot of useful information like links to user documentation, design documentation, mailing lists etc. can be found in the [resources](http://www.go.cd/community/resources.html) section.

## License

```plain
Copyright 2015 ThoughtWorks, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
