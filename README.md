Role Name
=========

Installs all software required for DXC OS build agent


To build, first you need a teamcity server running. I use this command:

docker run -d \
  -v teamcity_data:/data/teamcity_server/datadir \
  -v teamcity_logs:/opt/teamcity/logs  \
  -p 8111:8111 \
  --name teamcity-server-instance \
  jetbrains/teamcity-server:10.0.4