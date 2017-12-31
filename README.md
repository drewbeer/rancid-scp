# rancid-scp

Generic rancid support for pulling configs via scp, should work on anything.

# forked from https://github.com/schweikert/fnrancid-scp

License: Free as in beer

## Installation

1.   Enable scp on your Fortinet devices:


1.   Copy the 'rancid-scp' script to the location where the other rancid scripts
     are located.

1.   Make sure that it is executable:
     
        chmod +x rancid-scp

1.   Edit the file rancid.types.conf (add the following for the generic scp):
     
        genscp;script;rancid-scp

1.   Make sure that you have user and password stored in ~rancid/.cloginrc:

        add user       myhostname.mydomain   admin
        add password   myhostname.mydomain   {mypassword}
        add config-name myhostname.mydomain   /tmp/config.txt

     (note that hostname matching with wildcards doesn't work here, so put your full hostname in .cloginrc)

1.   Add your devices to router.db and use the type 'fortiscp'. For example:

        myhostname.mydomain;genscp;up

 
### notes:

i mainly use this for ubiquti airos devices, edgerouters, and some other misc places where i just want to make sure the config hasn't changed.


