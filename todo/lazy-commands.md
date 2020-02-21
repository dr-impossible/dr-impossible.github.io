# Installing commands the lazy way with docker

* I don't have the patience for python virtualenv, I like npm and bundler more
* docker images are self-contained and have the right dependencies
* docker offers isolation
* you can maintain separate runtime versions for each project
* you can limit network and disk access
* easiest way to run a database locally
* volumes vs. mounts
    * volumes preserve data
    * volumes are faster and good if you don't care to look at the files directly
    * volumes are good for databases
    * mounts are good for mounting source code, but slow on non-linux hosts