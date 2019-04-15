#os
FROM ubuntu:18.04

#update
RUN apt update && apt upgrade -y

#dependes
RUN apt install -y git nano npm nodejs curl

#meteor
RUN curl https://install.meteor.com/ | sh

#forbole
RUN cd /opt && mkdir gaia-bin && mkdir settings && git clone https://github.com/forbole/big_dipper.git

#initialize meteor
RUN cd /opt/big_dipper && meteor npm install --allow-superuser && meteor update --allow-superuser

CMD cd /opt/big_dipper && meteor --settings /opt/settings/settings.json --allow-superuser
