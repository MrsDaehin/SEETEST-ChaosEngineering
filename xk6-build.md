docker run --rm -it -u "$(id -u):$(id -g)" -v "${PWD}:/xk6" grafana/xk6 build v0.43.1 \
  --with github.com/grafana/xk6-kubernetes  \
  --with github.com/szkiba/xk6-yaml@latest
  --with github.com/mostafa/xk6-disruptor@latest 


  docker run --rm -it -u "$(id -u):$(id -g)" -v "${PWD}:/xk6" grafana/xk6 build v0.43.1 \
   --with github.com/mostafa/xk6-disruptor@latest 
   --output k6-disruptor


docker run --rm -it -u "$(id -u):$(id -g)" -v "$(pwd):/xk6" \
  grafana/xk6 build --with github.com/grafana/xk6-faker



WINDOWS

docker run --rm -e GOOS=windows -u "$(id -u):$(id -g)" -v "${PWD}:/xk6" `
  grafana/xk6 build  --output k6-faker.exe `
  grafana/xk6 build --with github.com/grafana/xk6-faker