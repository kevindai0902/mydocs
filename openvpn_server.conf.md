openvpn google-authenticator centos7


yum install epel-release


yum install openssh-server lzo openssl openssl-devel openvpn NetworkManager-openvpn openvpn-auth-ldap zip unzip google-authenticator  ntpdate easy-rsa net-tools bridge-utils


ntpdate tick.stdtime.gov.tw
ntpdate time.stdtime.gov.tw 
ntpdate clock.stdtime.gov.tw

0,30 * * * * /usr/sbin/ntpdate tick.stdtime.gov.tw > /dev/null 2>&1


[root@centos7 ~]# rpm -ql easy-rsa
/usr/share/doc/easy-rsa-3.0.6
/usr/share/doc/easy-rsa-3.0.6/COPYING.md
/usr/share/doc/easy-rsa-3.0.6/ChangeLog
/usr/share/doc/easy-rsa-3.0.6/README.md
/usr/share/doc/easy-rsa-3.0.6/README.quickstart.md
/usr/share/doc/easy-rsa-3.0.6/vars.example
/usr/share/easy-rsa
/usr/share/easy-rsa/3
/usr/share/easy-rsa/3.0
/usr/share/easy-rsa/3.0.6
/usr/share/easy-rsa/3.0.6/easyrsa
/usr/share/easy-rsa/3.0.6/openssl-easyrsa.cnf
/usr/share/easy-rsa/3.0.6/x509-types
/usr/share/easy-rsa/3.0.6/x509-types/COMMON
/usr/share/easy-rsa/3.0.6/x509-types/ca
/usr/share/easy-rsa/3.0.6/x509-types/client
/usr/share/easy-rsa/3.0.6/x509-types/code-signing
/usr/share/easy-rsa/3.0.6/x509-types/server
/usr/share/easy-rsa/3.0.6/x509-types/serverClient
/usr/share/licenses/easy-rsa-3.0.6
/usr/share/licenses/easy-rsa-3.0.6/gpl-2.0.txt


[root@centos7 ~]# rpm -ql openvpn
/etc/openvpn
/etc/openvpn/client
/etc/openvpn/server
/run/openvpn-client
/run/openvpn-server
/usr/lib/systemd/system/openvpn-client@.service
/usr/lib/systemd/system/openvpn-server@.service
/usr/lib/systemd/system/openvpn@.service
/usr/lib/tmpfiles.d/openvpn.conf
/usr/lib64/openvpn
/usr/lib64/openvpn/plugins
/usr/lib64/openvpn/plugins/openvpn-plugin-auth-pam.so
/usr/lib64/openvpn/plugins/openvpn-plugin-down-root.so
/usr/sbin/openvpn
/usr/share/doc/openvpn-2.4.8
/usr/share/doc/openvpn-2.4.8/AUTHORS
/usr/share/doc/openvpn-2.4.8/COPYING
/usr/share/doc/openvpn-2.4.8/COPYRIGHT.GPL
/usr/share/doc/openvpn-2.4.8/ChangeLog
/usr/share/doc/openvpn-2.4.8/Changes.rst
/usr/share/doc/openvpn-2.4.8/README
/usr/share/doc/openvpn-2.4.8/README.auth-pam
/usr/share/doc/openvpn-2.4.8/README.down-root
/usr/share/doc/openvpn-2.4.8/README.systemd
/usr/share/doc/openvpn-2.4.8/contrib
/usr/share/doc/openvpn-2.4.8/contrib/OCSP_check
/usr/share/doc/openvpn-2.4.8/contrib/OCSP_check/OCSP_check.sh
/usr/share/doc/openvpn-2.4.8/contrib/README
/usr/share/doc/openvpn-2.4.8/contrib/openvpn-fwmarkroute-1.00
/usr/share/doc/openvpn-2.4.8/contrib/openvpn-fwmarkroute-1.00/README
/usr/share/doc/openvpn-2.4.8/contrib/openvpn-fwmarkroute-1.00/fwmarkroute.down
/usr/share/doc/openvpn-2.4.8/contrib/openvpn-fwmarkroute-1.00/fwmarkroute.up
/usr/share/doc/openvpn-2.4.8/contrib/pull-resolv-conf
/usr/share/doc/openvpn-2.4.8/contrib/pull-resolv-conf/client.down
/usr/share/doc/openvpn-2.4.8/contrib/pull-resolv-conf/client.up
/usr/share/doc/openvpn-2.4.8/management-notes.txt
/usr/share/doc/openvpn-2.4.8/sample
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/README
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/client.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/firewall.sh
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/home.up
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/loopback-client
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/loopback-server
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/office.up
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/openvpn-shutdown.sh
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/openvpn-startup.sh
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/roadwarrior-client.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/roadwarrior-server.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/server.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/static-home.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/static-office.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/tls-home.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/tls-office.conf
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/xinetd-client-config
/usr/share/doc/openvpn-2.4.8/sample/sample-config-files/xinetd-server-config
/usr/share/doc/openvpn-2.4.8/sample/sample-scripts
/usr/share/doc/openvpn-2.4.8/sample/sample-scripts/auth-pam.pl
/usr/share/doc/openvpn-2.4.8/sample/sample-scripts/bridge-start
/usr/share/doc/openvpn-2.4.8/sample/sample-scripts/bridge-stop
/usr/share/doc/openvpn-2.4.8/sample/sample-scripts/ucn.pl
/usr/share/doc/openvpn-2.4.8/sample/sample-scripts/verify-cn
/usr/share/doc/openvpn-2.4.8/sample/sample-windows
/usr/share/doc/openvpn-2.4.8/sample/sample-windows/sample.ovpn
/usr/share/man/man8/openvpn.8.gz
/var/lib/openvpn

mkdir -p /etc/openvpn/easy-rsa/key

cp -r /usr/share/easy-rsa/3/* /etc/openvpn/easy-rsa/




cp /usr/share/doc/easy-rsa-3.0.6/vars.example  vars
 
 
vi vars    
 
set_var EASYRSA_REQ_COUNTRY     "TW"
set_var EASYRSA_REQ_PROVINCE    "Taiwan"
set_var EASYRSA_REQ_CITY        "New Taipei City"
set_var EASYRSA_REQ_ORG "DDIM Co"
set_var EASYRSA_REQ_EMAIL       "ddiminfra@gmail.com"
set_var EASYRSA_REQ_OU          "IT"

 [root@localhost easy-rsa]# ./easyrsa init-pki                                        #初始化pki，生成目录文件结构
init-pki complete; you may now create a CA or requests.
your newly created PKI dir is: /etc/openvpn/easy-rsa/pki
[root@localhost easy-rsa]# ls
easyrsa  openssl-1.0.cnf  pki  var  x509-types

./easyrsa build-ca nopass 
[root@localhost easy-rsa]# ./easyrsa build-ca   nopass                                    #创建ca证书
Note: using Easy-RSA configuration from: ./vars    

Enter PEM pass phrase:                                                                      #设置ca密码(我此处是写的silence)
Verifying - Enter PEM pass phrase:                                                     #再输一遍上面的密码


./easyrsa gen-req server nopass 


Keypair and certificate request completed. Your files are:
req: /etc/openvpn/easy-rsa/pki/reqs/server.req
key: /etc/openvpn/easy-rsa/pki/private/server.key

./easyrsa sign server server                    #第二个server是只上面服务端证书的CN名字，我们用的默认server,随便写

Note: using Easy-RSA configuration from: ./vars

Using SSL: openssl OpenSSL 1.0.2k-fips  26 Jan 2017


You are about to sign the following certificate.
Please check over the details shown below for accuracy. Note that this request
has not been cryptographically verified. Please be sure it came from a trusted
source or that you have verified the request checksum with the sender.

Request subject, to be signed as a server certificate for 1080 days:

subject=
    commonName                = server


Type the word 'yes' to continue, or any other input to abort.
  Confirm request details: yes
Using configuration from /etc/openvpn/easy-rsa/pki/safessl-easyrsa.cnf
Enter pass phrase for /etc/openvpn/easy-rsa/pki/private/ca.key:
Check that the request matches the signature
Signature ok
The Subject's Distinguished Name is as follows
commonName            :ASN.1 12:'server'
Certificate is to be certified until Feb 25 06:59:33 2023 GMT (1080 days)

Write out database with 1 new entries
Data Base Updated

Certificate created at: /etc/openvpn/easy-rsa/pki/issued/server.crt

[root@centos7 easy-rsa]#
./easyrsa gen-dh 
