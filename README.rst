=====================================================
Script for OpenDnssec to fully automate keys rollover
=====================================================

/*\ Under developement /*\
--------------------------

Install
-------

    cd /etc/openddnssec
    git clone https://github.com/sileht/ovh-ds.git
    cd ovh-ds
    virtualenv venv
    venv/bin/pip install -r requirements.txt

OVH API credentials configuration
---------------------------------

    cp ovh.conf.sample ovh.conf
    vi ovh.conf

Test OVH API access, should print all your ds records

    ./ovh-ds list


Opendnssec configuration
------------------------

In /etc/opendnssec/conf.xml set :

    <DelegationSignerSubmitCommand>/etc/opendnssec/ovh-ds/ovh-ds.wrapper</DelegationSignerSubmitCommand>
