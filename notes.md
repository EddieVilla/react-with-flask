demo:
curl http://localhost:5000/api/time

to run on WAN and not just localhost:
npm run dev -- --host 0.0.0.0

fresh container:
docker run -it -p 5173:5173 ubuntu:24.04 bash

commands to run inside container. move to script:
```
apt update
cd root/
DEBIAN_FRONTEND=noninteractive TZ=Etc/UTC apt-get install -y python3 python3.12-venv curl git vim

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
\. "$HOME/.nvm/nvm.sh"
nvm install 24
git clone https://github.com/EddieVilla/react-with-flask.git
cd react-with-flask/
npm install
cd api
python3 -m venv venv
source venv/bin/activate
pip install -r ../requirements.txt
cd ..

npm run api &
curl http://localhost:5000/api/time
npm run dev -- --host 0.0.0.0
```
