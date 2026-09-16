## Summary

OS2borgerPC’s client API at `/client-api/` accepts requests without authentication. An attacker who can reach the admin portal over the network can impersonate a client device using MAC-based identity and submit control instructions. This can lead to full compromise of kiosk machines with root privileges.

## Description

A critical vulnerability exists in the OS2borgerPC administration platform due to missing authentication in the client API endpoint `/client-api/`. The API accepts client control requests without username/password, and device identity is derived only from MAC address, which is not a secret.

As a result, an unauthorized actor can take over a kiosk device, execute arbitrary code as root, and establish persistent compromise. Affected kiosks may be misused to capture citizen-entered data, display manipulated content, or participate in botnet activity. The weakness is architectural and affects installations across forks where the relevant fix is not present.

There are no reliable indicators of compromise (IOCs) or logging artifacts that can conclusively confirm or rule out past exploitation.

## Impact

An unauthenticated remote attacker can obtain full control of kiosk devices and run code with highest privileges. Potential impact includes:

1. Exposure of data entered by citizens on kiosks.
2. Manipulation of user-facing kiosk content.
3. Persistent malware installation on endpoints.
4. Repeated compromise across the fleet.

## Affected Versions
os2borgerpc-admin-site < 7.1.0
os2borgerpc-client < 2.7.0

## Patched Versions
os2borgerpc-admin-site 7.1.0
os2borgerpc-client  2.7.0


## Recommended Remediation Sequence

1. Close exposure first: upgrade the admin portal.
2. Reinstall the kiosk fleet as a precaution.
3. Rotate the device admin password and other keys/secrets stored on kiosk devices and review unknown device registrations and configuration changes.

## Status / Roadmap

Fixed

## Credits

OS2 security coordination and maintainers/contributors.