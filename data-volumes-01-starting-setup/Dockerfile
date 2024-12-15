FROM node

WORKDIR /APP

COPY package.json /APP

RUN npm install

# .dockerignore 에 있는 폴더, 파일은 컨테이너 내부로 복사되지 않음
COPY . /APP

# layer 기반이라 npm install 같이 불필요한 작업 뒤에서 선언 하는게 좋음
ARG DEFAULT_PORT=80

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

#VOLUME ["/APP/node_modules"]

VOLUME ["/APP/feedback"]

CMD [ "npm", "start" ]

# Volume name을 지정해야 하는 이유: 여러 컨테이너가 volume을 공유할 수 있도록 하기 위해서
