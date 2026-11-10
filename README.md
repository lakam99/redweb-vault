# RedWeb Vault

Windows installers and the automatic update feed for RedWeb Vault.

[Download the latest installer](https://github.com/lakam99/redweb-vault/releases/latest)

RedWeb Vault hosts file collections on your own PC. Invite individual people, set permitted upload formats, quotas and expiry, and revoke access when needed. Guest uploads pass content validation on the PC before they reach their collection folder.

Supported formats: PNG, JPEG, WebP, UTF-8 text, JSON, and ZIP. The validator rejects disguised executables, malformed content, unsafe archive paths, nested/encrypted ZIPs and excessive archive expansion. Images and accepted archives are rebuilt. Format validation is not an antivirus scan.

Version 0.3.0 adds dark mode (Light/Dark/System), direct one-link invitations without passwords, and dropdowns for collection capacity, maximum file size, and upload quotas. Existing private invitation links retain their permissions and work without their previous passwords. Anyone holding a complete link can use its assigned access until expiry or revocation.

Internet sharing uses an outbound authenticated data tunnel to Google Cloud. The desktop opens the connections; the cloud streams traffic through them to the app's internal loopback service. File validation and storage stay on the PC. No local reverse proxy, public PC address, port forwarding, or inbound firewall rule is required in tunnel mode. Pairing requires the relay owner's private key. The PC must remain awake and hosting. Direct LAN operation is also available with the tunnel disabled.

The application checks for updates after startup and every six hours. Updates download in the background; select **Settings → Application updates → Restart & install update** to apply them. Hosting stops before installation. Version 0.1.0 users must install the latest version once to enable this update mechanism.

Installers are currently unsigned. The updater uses the HTTPS GitHub release feed and verifies the downloaded artifact checksum. Keep control of the GitHub release account and repository.

This repository contains the public distribution and update feed. It does not contain the application source, private relay pairing keys, or user files.
