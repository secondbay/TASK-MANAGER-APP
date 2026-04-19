# ambil base envi dari node.js
FROM node:18

# set container directory
WORKDIR /app

# salin dan install depedensi ke container directory
COPY package*.json ./
RUN npm ci --only=production	

# salin source code ke container directory
COPY . .

# expose port backend
EXPOSE 5000

# perintah untuk menjalankan app
CMD ["npm","start"]
