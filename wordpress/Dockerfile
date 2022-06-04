FROM wordpress

ARG version=2.2.0
RUN curl -LJO https://github.com/Teplitsa/kandinsky/archive/refs/tags/v${version}.tar.gz

RUN tar -xzf kandinsky-${version}.tar.gz -C /var/www/html/wp-content/themes
