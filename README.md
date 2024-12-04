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
  
- Interfaces - Assignments
  - Assign a new interface
    - Device
      ```
      {WireGuard interface}
      ```
    - Description
      ```
      WG0
      ```
    - Add
    - Save
      
- Interfaces - WG0
  - Enable interface
  - Prevent interface removal
  - Save
  - Apply changes
    
- Firewall - Rules - WAN
  - Add
    - Action
      ```
      Pass
      ```
    - Interface
      ```
      WAN
      ```
    - Protocol
      ```
      UDP
      ```
    - Source
      ```
      any
      ```
    - Destination
      ```
      WAN Address
      ```
    - Destination port range
      - from
        ```
        51820
        ```
      - to
        ```
        51820
        ```
    - Description
      ```
      Allow wireguard traffic
      ```
    - Save
  - Apply changes




## WIREGUARD - CLIENT
