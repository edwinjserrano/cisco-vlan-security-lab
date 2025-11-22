# Cisco VLAN Security Lab

Este repositorio documenta un laboratorio de seguridad en Cisco IOS con ACLs extendidas, DHCP y SSHv2.

## Características
- ACLs por VLAN (10–70, Voice) con permisos específicos (HTTP/HTTPS, ICMP, DHCP).
- Bloqueo de Telnet y tráfico no autorizado entre VLANs.
- ACL exclusiva para SSH: solo la red 192.168.6.0/24 puede iniciar sesión.
- Generación de claves RSA y activación de SSH versión 2 en router y switches.
- DHCP pools configurados en R1 para cada VLAN.
- Seguridad adicional en switches: DHCP snooping, ARP inspection, port-security, spanning-tree BPDU guard.

## Verificación
- `show access-lists` → contadores incrementan en tráfico permitido.
- `ping` desde 192.168.6.0/24 → éxito.
- `ssh` desde 192.168.6.0/24 → éxito.
- `telnet` desde cualquier VLAN → bloqueado.
- Clientes → reciben IP automáticamente vía DHCP.

---

# Cisco VLAN Security Lab (EN)

This repository documents a Cisco IOS security lab with extended ACLs, DHCP, and SSHv2.

## Features
- VLAN-based ACLs (10–70, Voice) with specific permits (HTTP/HTTPS, ICMP, DHCP).
- Telnet blocked and unauthorized inter-VLAN traffic denied.
- Dedicated SSH ACL: only 192.168.6.0/24 can initiate sessions.
- RSA key generation and SSH version 2 enabled on router and switches.
- DHCP pools configured on R1 for each VLAN.
- Additional switch security: DHCP snooping, ARP inspection, port-security, spanning-tree BPDU guard.

## Verification
- `show access-lists` → counters increment on permitted traffic.
- `ping` from 192.168.6.0/24 → success.
- `ssh` from 192.168.6.0/24 → success.
- `telnet` from any VLAN → blocked.
- Clients → automatically obtain IP via DHCP.
