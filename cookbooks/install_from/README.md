# install_from chef cookbook

Installs/Configures install_from

* Cookbook source:   [http://github.com/infochimps-cookbooks/install_from](http://github.com/infochimps-cookbooks/install_from)
* ClusterChef tools: [http://github.com/infochimps/cluster_chef](http://github.com/infochimps/cluster_chef)
* Homebase (shows cookbook in use): [http://github.com/infochimps-labs/cluster_chef-homebase](http://github.com/infochimps-labs/cluster_chef-homebase)

## Overview

Does the fetch-unpack-configure-build-install dance.

Given a project `pig`, with url `http://apache.org/pig/pig-0.8.0.tar.gz`, and
the default :prefix_root of `/usr/local`, this provider will

* fetch  it to :package_file (`/usr/local/src/pig-0.8.0.tar.gz`)
* unpack it to :install_dir  (`/usr/local/share/pig-0.8.0`)
* create a symlink for :home_dir (`/usr/local/share/pig`) pointing to :install_dir
* configure the project
* build the project
* install the project

## Recipes 

* `default`                  - Base configuration for install_from

## Integration

Supports platforms: debian and ubuntu



## Attributes

* `[:install_from][:apache_mirror]`   - Default Apache mirror to use (default: "http://apache.mirrors.tds.net")
  - Choose one of the [Apache project mirrors](http://www.apache.org/dyn/closer.cgi) -- omit the trailing '/'s. The token `:apache_mirror:` (note : at end of token) in a `release_url` attribute will be replaced by this base; see the pig recipe for an example.

## License and Author

Author::                Philip (flip) Kromer - Infochimps, Inc (<coders@infochimps.com>)
Copyright::             2011, Philip (flip) Kromer - Infochimps, Inc

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

> readme generated by [cluster_chef](http://github.com/infochimps/cluster_chef)'s cookbook_munger