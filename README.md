# RedWeb Vault

Windows installers and the automatic update feed for RedWeb Vault.

[Download the latest installer](https://github.com/lakam99/redweb-vault/releases/latest)

RedWeb Vault hosts file collections on your own PC. Invite individual people, set permitted upload formats, quotas and expiry, and revoke access when needed. Guest uploads pass content validation on the PC before they reach their collection folder.

Supported formats: PNG, JPEG, WebP, UTF-8 text, JSON, and ZIP. The validator rejects disguised executables, malformed content, unsafe archive paths, nested/encrypted ZIPs and excessive archive expansion. Images and accepted archives are rebuilt. Format validation is not an antivirus scan.

Version 0.2.0 adds an HTTPS Google Cloud relay and GitHub Releases updates. The relay passes traffic to a paired PC; file validation and storage stay on that PC. Pairing requires a private key supplied by the relay owner. The PC must stay awake and hosting. LAN-only operation is also available.

The application checks for updates after startup and every six hours. Updates download in the background; select **Settings → Application updates → Restart & install update** to apply them. Hosting stops before installation. Version 0.1.0 users must install version 0.2.0 once to enable this update mechanism.

Installers are currently unsigned. The updater uses the HTTPS GitHub release feed and verifies the downloaded artifact checksum. Keep control of the GitHub release account and repository.

This repository contains the public distribution and update feed. It does not contain the application source, private relay pairing keys, or user files.
