# proxmox

# wyłączenie komunikatu o braku subskrypcji
# wchodzimy w shell proxmox i wpisujemy:

sed -i.backup -z "s/res === null || res === undefined || \!res || res\n\t\t\t.data.status.toLowerCase() \!== 'active'/false/g" /usr/share/javascript/proxmox-widget-toolkit/proxmoxlib.js && systemctl restart pveproxy.service

