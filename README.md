# apache_superset

# clone repository
git clone https://github.com/apache/superset.git
cd superset

#generate private key
openssl rand -base64 42

# open File docker/.env and find or add to the end variable SUPERSET_SECRET_KEY:
SUPERSET_SECRET_KEY=ваш_сгенерированный_ключ_из_openssl

# go to the root of repository
cd ..

# start superset from image
TAG=latest docker compose -f docker-compose-image-tag.yml up -d

# open in browser: http://localhost:8088
	• login: admin
	• password: admin
