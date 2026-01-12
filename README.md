Nessus and Nmap (Target: 10.0.3.4 – Windows PC)

Nessus (Vulnerability Scan)

Nessus performed a Basic Network Scan against 10.0.3.4 and returned a list of identified weaknesses.

Key findings from your screenshots include:

Critical: Unsupported Windows OS (remote) — the host is running an unsupported Windows version (Windows 8.1), which increases risk because security updates may be missing.

High: MS17-010 (SMB / EternalBlue-related) — indicates serious SMB vulnerabilities commonly associated with WannaCry/EternalBlue-era issues if not patched.

Medium: SMB Signing not required — increases risk of man-in-the-middle style attacks on SMB traffic.

You also have multiple Info findings (service/OS fingerprints, SMB detection, enumeration items) that help with asset visibility.

Nmap (Port Scan)

Nmap was used to discover open ports and identify services running on 10.0.3.4 (what is reachable on the network).

In practical terms, Nmap answers:

“Which ports are open?”

“What services/versions are listening?”

“Is the host up and what OS/service fingerprints can we detect?”

Based on what Nessus already confirmed, SMB is reachable (TCP/445) on the target — Nmap would typically show 445/tcp open (and possibly other Windows-related ports depending on configuration).
