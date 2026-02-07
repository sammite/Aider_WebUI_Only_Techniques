# aider_dockerized_enhancements
Just my personal mods to the docker version of aider

run with:


```
sudo docker run -it \
    --user $(id -u):$(id -g) \
    --network host \
    --volume $(pwd):/app \
    --env DISPLAY=$DISPLAY \
    --env OLLAMA_API_BASE=http://localhost:11434 \
    --volume /tmp/.X11-unix:/tmp/.X11-unix \
    aider-xclip \
    --no-check-update \
    --model ollama/llama3 \
    --copy-paste

```

in conjunction with locallama to properly copy paste in and out of a docker. 
