FROM tutum/lamp:latest
MAINTAINER George Dawoud <george@dawouds.com>

# Download latest version of ChurchInfo into /app
RUN rm -fr /app && git clone https://github.com/ChurchCRM/CRM.git /app

# Add database setup script
ADD setup_mysql.sh /setup_mysql.sh
RUN chmod 755 /*.sh

EXPOSE 80 3306
CMD ["/run.sh"]
