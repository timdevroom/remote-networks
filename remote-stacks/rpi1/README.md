# docs
run the command below to allow ip forwarding

[tailscale-docs] (https://tailscale.com/docs/features/subnet-routers?tab=linux#enable-ip-forwarding)

```bash
echo 'net.ipv4.ip_forward = 1' | sudo tee -a /etc/sysctl.d/99-tailscale.conf
echo 'net.ipv6.conf.all.forwarding = 1' | sudo tee -a /etc/sysctl.d/99-tailscale.conf
sudo sysctl -p /etc/sysctl.d/99-tailscale.conf
```