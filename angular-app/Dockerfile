FROM node:alpine AS my-app-build
WORKDIR /app
COPY . .
RUN npm install && npm run build

# stage 2

FROM nginx:alpine
COPY --from=my-app-build /app/dist/angular-app /usr/share/nginx/html
