# Configuring UFW for instances to only allow traffic from load balancer

```bash
sudo ufw allow ssh
```

```bash
sudo ufw allow from <VM3_PUBLIC_IP> to any port 80
```

```bash
sudo ufw deny 80
```

| To          | Action | From          |
| ----------- | ------ | ------------- |
| 22/tcp      | ALLOW  | Anywhere      |
| 8010        | ALLOW  | 10.211.55.13  |
| 8020        | ALLOW  | 10.211.55.13  |
| 8010        | DENY   | Anywhere      |
| 8020        | DENY   | Anywhere      |
| 22/tcp (v6) | ALLOW  | Anywhere (v6) |
| 8010 (v6)   | DENY   | Anywhere (v6) |
| 8020 (v6)   | DENY   | Anywhere (v6) |
