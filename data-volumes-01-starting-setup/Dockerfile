FROM node

WORKDIR /APP

COPY package.json /APP

RUN npm install

# .dockerignore 에 있는 폴더, 파일은 컨테이너 내부로 복사되지 않음
COPY . /APP

EXPOSE 80

#VOLUME ["/APP/node_modules"]

VOLUME ["/APP/feedback"]

CMD [ "npm", "start" ]

# Volume name을 지정해야 하는 이유: 여러 컨테이너가 volume을 공유할 수 있도록 하기 위해서
