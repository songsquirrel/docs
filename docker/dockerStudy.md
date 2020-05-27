### demo
1. define a container with dockerfile
2. build a image
> docker build --tag ${imageName}:${imageVersion}
3. run image as a container
> docker run --publish 8000:8080 --detach bb ${imageName}:${imageVersion}
> --publish asks Docker to forward traffic incoming on the host’s port 8000, to the container’s port 8080. Containers have their own private set of ports, so if you want to reach one from the network, you have to forward traffic to it in this way. Otherwise, firewall rules will prevent all network traffic from reaching your container, as a default security posture.
> --detach asks Docker to run this container in the background.
> --name specifies a name with which you can refer to your container in subsequent commands, in this case bb.
4. remove/stop a running container
    docker rm --force bb/docker stop bb

5. 删除容器

  docker rm -f {containerID}

6. 导出/导入容器快照

    docker export {containerID} > fileName.tar

    docker import $URL/PATH  [repository[:tag]]

7. 进入容器命令

    ```shell
    # 退出会导致容器终止
    docker attach $containerID
    # 退出容器仍会继续运行
    docker exec $containerID
    ```

8. 



