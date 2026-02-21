
    grep -q routerich /etc/opkg/customfeeds.conf || echo src/gz routerich https://github.com/routerich/packages.routerich/raw/24.10.4/routerich >> /etc/opkg/customfeeds.conf
    
    wget https://github.com/routerich/packages.routerich/raw/main/routerich.pub -O /tmp/routerich.pub && opkg-key add /tmp/routerich.pub
    
    opkg update

    wget --no-check-certificate -O /tmp/universal_config_new_podkop.sh https://raw.githubusercontent.com/alexsdav/WBR3000UAXv1/refs/heads/main/universal_config_new_podkop.sh && chmod +x /tmp/universal_config_new_podkop.sh && /tmp/universal_config_new_podkop.sh $1 $2

info

    wget --no-check-certificate -O /tmp/universal_config_new_podkop1.sh https://raw.githubusercontent.com/alexsdav/WBR3000UAXv1/refs/heads/main/universal_config_new_podkop1.sh && chmod +x /tmp/universal_config_new_podkop1.sh && /tmp/universal_config_new_podkop1.sh $1 $2
