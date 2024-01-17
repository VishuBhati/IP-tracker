# IP-tracker

import nmap3

nmap=nmap3.Nmap()

class network(object):
            def __init__(self,ip):
                        ip=raw_input("Enter a default IP is socks5//127.0.0.1:9050")
                        self.ip=ip

            def networkscanner(self):
                        if len(self.ip)==0:
                                    network='socks5//127.0.0.1:9050'
                        else:
                                    network=self.ip+'/24'

                        print("Scanning please wait..........")

                        nm=nmap3.portscanner()
                        nm.scan(hosts=network,arguments='-sn')
                        host_list=[(x,nm[x]['status']['state'])for x in nm.all_hosts()]
                        for host, status in host_list():
                                    print("Host/t()".format(host))

if __name__=='__main__':
            D=network()
            d.networkscanner()
