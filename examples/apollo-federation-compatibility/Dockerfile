FROM node:19
WORKDIR /web
COPY package.json products.graphql tsconfig.json codegen.yaml ./
RUN npm install
COPY src ./src
RUN npm run build
EXPOSE 4001
USER node
CMD node dist/index.js
