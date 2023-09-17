FROM nginx

RUN apt-get update && apt-get upgrade -y

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]

LABEL App="nginx"
LABEL Environment="Development"