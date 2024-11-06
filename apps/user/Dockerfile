# 사용할 이미지
FROM node:alpine AS development

WORKDIR /usr/src/app

# package.json 복사해오기
COPY package*.json ./

COPY pnpm-lock.yaml ./

# PNPM 설치하기
RUN npm i -g pnpm

# Dependency 설치하기
RUN pnpm i

# 나머지 파일, 폴더 복사해오기
COPY . .

CMD ["pnpm" ,"start:dev" , "user"]