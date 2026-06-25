FROM node:22-alpine

WORKDIR /app

# เคลียร์ Cache ของ npm เพื่อความชัวร์ป้องกันปัญหาเดิมค้าง
RUN npm cache clean --force

COPY package*.json ./

# ใช้ npm ci หรือเพิ่มสิทธิ์เพื่อป้องกันการพังของ optional dependencies
RUN npm install

COPY . .

# สั่งทำการ Build สภาพแวดล้อม Next.js สำหรับ Production
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
