# optixtest
opengl optix test project running on docker via visual studio cross platform.
Including a testcodes and visual studio environment.

The docker comes from nvdia-cudagl, install cuda+optix+opengl+GLFW+GLEW+Visual Studio cross platform support, must run under the nvidia-docker2 run-time. No docker file. 

Use command: 
docker run --name=optix-x11 --runtime=nvidia --net=host --env="DISPLAY" --volume="$HOME/.Xauthority:/root/.Xauthority:rw" --volume="$HOME/document/projects:/root/projects/:rw" -it gzfrozen/env:0.4
to run a container which can build(if you wish) and see GUI applications.

Use command: 
docker run --name=optix-vs --runtime=nvidia --security-opt seccomp:unconfined -p 12345:22 --volume="$HOME/document/projects:/root/projects/:rw" -d gzfrozen/env:0.4 /usr/sbin/sshd -D
to run a container which can be accessed and debug and build by visual studio, however can't see GUI windows.

You can run two containers in the same time and all the source codes and build files will be sychronized.
