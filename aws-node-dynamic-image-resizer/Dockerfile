FROM amazonlinux:2.0.20240223.0
WORKDIR /deploy
RUN yum -y install make gcc*
RUN curl --silent --location https://rpm.nodesource.com/setup_8.x | bash -
RUN yum -y install nodejs
RUN npm install -g serverless
COPY . .
RUN npm i --production

RUN ["chmod", "+x", "deploy.sh"]
CMD ./deploy.sh ; sleep 2m
