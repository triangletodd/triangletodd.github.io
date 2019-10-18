###
# Builder
###
FROM jekyll/builder:3.8 as base
COPY . /srv/jekyll/
RUN jekyll build

###
# Runtime
###
FROM nginx
EXPOSE 80
COPY --from=base /srv/jekyll/_site /usr/share/nginx/html/
