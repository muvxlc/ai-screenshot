FROM node:18-alpine

WORKDIR /app

# คัดลอกเฉพาะไฟล์ package เพื่อทำ Layer Caching ช่วยให้ Build ไวขึ้นในครั้งถัดไป
COPY package*.json ./
RUN npm install --production

# คัดลอกโค้ดทั้งหมด
COPY . .

EXPOSE 5000

CMD ["npm", "start"]
