# OPNsense - WireGuard - Road Warrior

## WIREGUARD - HOST
- VPN - WireGuard - Instances
  - Add
    - Name
      ```
      WG0
      ```
    - Generate new keypair
    - Listen port
      ```
      51820
      ```
    - Tunnel address
      ```
      10.49.0.1/24
      ```
    - Save
      
- VPN - WireGuard - Peers
  - Add
    - Name
      ```
      WG1
      ```
    - Public key
      ```
      {The WG public key of the client}
      ```    
    - Allowed IPs
      ```
      10.49.0.2/32
      ```
    - Endpoint address
      ```
      {Public IP address of the OPNsense host}
      ```
    - Endpoint port
      ```
      51820
      ```
    - Instances
      ```
      WG0
      ```
    - Keepalive interval
      ```
      25
      ```
    - Save
      
- Enable WireGuard




## WIREGUARD - CLIENT
