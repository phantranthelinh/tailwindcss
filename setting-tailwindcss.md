

npm init -y

npm install -D tailwindcss@latest postcss@latest autoprefixer@latest


npx tailwindcss init -p

3. Tạo file src/style.css
@tailwind base;
@tailwind components;
@tailwind utilities;
4. Ghi đè nội dung file package.json
{
  "name": "tailwind",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "dev": "vite",
    "watch":"npx tailwindcss -i ./src/main.css -o ./build/style.css --watch" 
  },
  "devDependencies": {
    "autoprefixer": "^10.3.4",
    "postcss": "^8.3.6",
    "tailwindcss": "^3.0.0"
  }
}
5. Ghi đè nội dung file tailwind.config.js
module.exports = {
  content: [
   "**/*.html","./src/**/*.{html,css,js}"
  ],
  darkMode: 'class', // or 'media' or 'class'
  theme: {
    extend: {},
  },
  variants: {
    extend: {},
  },
  plugins: [],
}
6. Dịch file
npm run watch

Giữ cho lệnh này chạy, không tắt terminal
