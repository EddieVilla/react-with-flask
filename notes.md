demo:
curl http://localhost:5000/api/time

to run on WAN and not just localhost:
npm run dev -- --host 0.0.0.0

fresh container:
docker run -it -p 5173:5173 ubuntu:24.04 bash

