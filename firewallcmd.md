# Firewall cmd

```bash
# To list all port
sudo firewall-cmd --list-all

# Allow port permanently
sudo firewall-cmd --add-port=3000/tcp --permanent

# reload configuration
sudo firewall-cmd --reload
```
