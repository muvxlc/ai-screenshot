FROM node:22-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install --production

COPY . .

EXPOSE 5000

# เปลี่ยนจาก npm start มาเรียกใช้ node รันไฟล์หลักโดยตรง
CMD ["npm", "start"]
