https://code-adda.com/2018/05/deploy-angular-app-on-tomcat-server/    ---- Try with this 


I have tried in this Method

FROM node:8.11.4
ENV proxy=http://cis-india-pitc-bangalorez.proxy.corporate.ge.com:80
ENV proxy=https://cis-india-pitc-bangalorez.proxy.corporate.ge.com:80

WORKDIR app
COPY edge-app-ui/* /app
RUN npm i yarn
RUN yarn global add @angular/cli@latest
RUN ng build --configuration=staging
RUN ng build -prod



MY Alpine Image is 

registry.gear.ge.com/predixmachine/openjdk-jre-x86_64  -- 
