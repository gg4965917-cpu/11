# вибираємо офіційний образ Node.js
FROM node:18-alpine

# встановлюємо робочу директорію
WORKDIR /app

# копіюємо package.json та package-lock.json (якщо є)
COPY package*.json ./

# встановлюємо залежності
RUN npm install --production

# копіюємо весь код
COPY . .

# збираємо (якщо маєш билд-скрипт)
# RUN npm run build  〈— закоментуй або розкоментуй, якщо потрібно

# вказуємо порт, який слухає застосунок
ENV PORT=3000

# хочемо, щоб застосунок слухав порт із process.env.PORT
EXPOSE 3000

# команда запуску (припускаємо, що у тебе є скрипт start)
CMD ["npm", "start"]
