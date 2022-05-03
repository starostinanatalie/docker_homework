from node:16-alpine as builder
workdir /frontend
copy . ./
run npm install
run npm run build

from nginx:alpine
copy --from=builder /frontend/build /usr/share/nginx/html

