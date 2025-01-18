FROM node 
WORKDIR /app
COPY frontend/package.json .
RUN npm install
COPY /frontend .
CMD ["node", "app.js"]