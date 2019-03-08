# Synology DiskStation 
### Startup Script
This is a example and a skeleton on how to create a startup script for Synology DiskStation and make it executable.

#### Compatibility
Tested on DS918+ running on version DSM 6.2.1-23824 Update 6

#### Script
As `root`, copy and paste the following
```bash
cat << \EOF > /usr/local/etc/rc.d/S99example.sh
#!/bin/sh
# S99example.sh

case $1 in
start)
        echo "Starting..."
        ;;
stop)
        echo "Stopping..."
        ;;
*)
        echo "Usage: $0 [start|stop]"
        ;;
esac
EOF

chmod 755 /usr/local/etc/rc.d/S99example.sh
```
