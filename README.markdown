__eipclean__

_Clean spurious elastic IP entries from cloud hypervisors._

Output of some sample runs:
 </br>
_Non-verbose, dry run mode, on a configuration that requires no changes:_ </br>
`[root@linux bin]# ./eipclean -d  -c zoochannel1 -i 192.168.3.20` </br>
`192.168.3.20 owner: hyper-6` </br>
`Running in dry run mode.  No changes will be made to EIP config on any hypervisor.` </br>
`CORRECT CONFIG: EIP 192.168.3.20 has an owner and is configured on a single hyper.` </br>
`[root@linux bin]#` </br>
 </br>
_No options, defaults to -h help message:_ </br>
`[root@linux bin]# ./eipclean` </br>
`Usage: eipclean [options] -c zookeeper_channel -i eip ...` </br>
`    -c, --channel CHANNEL            (Required) zookeeper channel` </br>
`    -i, --ip EIP                     (Required) elastic IP address` </br>
`    -v, --verbose                    Output verbose information` </br>
`    -d, --dryrun                     Do a dry run (don't actually change anything)` </br>
`    -h, --help                       Show this message` </br>
`[root@linux bin]#` </br>
 </br>
_Verbose, dry run mode, on a configuration that requires no changes:_ </br>
`[root@linux bin]# ./eipclean -d -v -c zoochannel1 -i 192.168.3.20` </br>
`192.168.3.20 owner: hyper-6` </br>
`Running in dry run mode.  No changes will be made to EIP config on any hypervisor.` </br>
`hyper-1: ` </br>
`hyper-2: ` </br>
`hyper-3: ` </br>
`hyper-4: ` </br>
`hyper-5: ` </br>
`hyper-6:     inet 192.168.3.20/32 scope global br0` </br>
`hyper-7: ` </br>
`hyper-8: ` </br>
`hyper-9: ` </br>
`hyper-10: ` </br>
`CORRECT CONFIG: EIP 192.168.3.20 has an owner and is configured on a single hyper.` </br>
`[root@linux bin]#` </br>
