FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

# สั่งทำการ Build สภาพแวดล้อม Next.js สำหรับ Production
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
