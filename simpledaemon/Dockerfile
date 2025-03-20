# https://indeed.atlassian.net/wiki/spaces/PURE/pages/155582616/Get+your+feet+wet+Deploy+a+Simple+Python+Script+as+a+Kubernetes+Cronjob
FROM nginxinc/nginx-unprivileged
 
RUN mkdir -p /usr/local/devops/bin
ADD runGo.sh /usr/local/devops/bin/
RUN mkdir -p /usr/share/nginx/html/private/
ADD healthcheck /usr/share/nginx/html/private/
ADD current_version.txt /usr/share/nginx/html/private/
RUN mkdir -p /usr/share/nginx/html/info
ADD healthcheck /usr/share/nginx/html/info

CMD [ "/usr/local/devops/bin/runGo.sh"]
