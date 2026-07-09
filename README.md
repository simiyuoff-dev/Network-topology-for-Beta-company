# Network-topology-for-Beta-company
This is a three tier architecture,goal to make it redudant

I have created a network topology for beta enterprise,it has five departments , finance, HR, sales and IT,it works remotely.
I have  three routers from the isp router, branch router ,remote router and the head-quater router
It is the first day i have configured the routers for branch,hq and remote, i have set the hostname using the 'hostname' password 'enable secret ''' for router CLI access,also set password to access the routers via console using 'line console 0' ,'password ''','login','exit' . to make all the password not to be showd in plain text i have run 'service password-encyption',
I have enable ssh using commands 'ip  domain-name beta.local' 'username '' password ''' then 'crypto key generate rsa' then locking the VTY lines to use ssh, then prompt to enter modulus size this turn on ssh.Then 'line vty 0 4' meaning it has a maximum of 4 ssh access at the same time,'transport input ssh' to enable ssh only, 'login local' to check pair username/password instead of shared line password.
i have done this to all routers except the isp which i encrypted the cli access only.
Then i has set banner message of the day 'banner motd 'for info about prohibited access. i have made sure to run 'copy running-config startup-config' to mantain the configs even after router shut-down.
Here is the topology. [secondphase]
