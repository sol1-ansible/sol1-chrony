# sol1-chrony
Basic role to install and maintain Chrony configuration for clients and/or servers.

By default the role will deploy using the AU NTP pool list as the servers.
If chrony_allowed_networks varible is defined, it will deploy and allow hosts to from the chrony_allowed_networks list to poll it for time and act as a server.

Notes:
If configuring server and clients, set chrony_allowed_networks and chrony_upstream_servers in group_vars for the servers. Then set the server IP/Hostname of your servers in chrony_upstream_servers in group_vars for the clients. 
