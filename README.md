# optixtest
opengl optix test project running on docker via visual studio cross platform.
Including a testcodes and visual studio environment.

The docker comes from nvdia-cudagl, install cuda+optix+opengl+GLFW+GLEW+Visual Studio cross platform support, must run under the nvidia-docker2 run-time. No docker file. 
Use command: 
docker run --name=optix-vs --runtime=nvidia --security-opt seccomp:unconfined -p 12345:22 -d gzfrozen/env:0.4 /usr/sbin/sshd -D 
to run a container which can access by hostaddress:12345. 
