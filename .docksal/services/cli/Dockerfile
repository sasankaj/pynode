# Use a stock Docksal image as the base
FROM docksal/cli:latest

# Install additional global npm dependencies
RUN set -e; \
	# Initialize nvm environment
	. $NVM_DIR/nvm.sh; \
	# Install packages
	npm install -g nodemon;


# Install python and Django
WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "./your-daemon-or-script.py" ]
