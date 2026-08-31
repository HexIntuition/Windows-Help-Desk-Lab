# Ticket 01 — DNS Resolution Failure

> **Lab disclosure:** This is a simulated Windows help desk scenario created for hands-on troubleshooting practice. It is not a real customer incident.

## Reported issue

The workstation appeared connected to the network, but websites could not be reached by hostname. Firefox returned a **Server Not Found** error for `google.com`.

## Troubleshooting

1. Confirmed the browser could not reach `google.com`.
2. Reviewed the workstation network configuration with `ipconfig /all`.
3. Tested raw IP connectivity with `ping 1.1.1.1`; the ping succeeded, showing that basic IP connectivity was working.
4. Tested name resolution with `nslookup google.com`; the DNS request timed out.
5. Identified the configured DNS server as `203.0.113.1`, intentionally set as a non-working DNS value for this lab.

## Root cause

The workstation had an incorrect DNS server configured. Network connectivity was available, but hostname resolution was failing.

## Resolution

Changed the preferred IPv4 DNS server to the known-good public resolver `8.8.8.8`, then cleared the local DNS resolver cache with:

```cmd
ipconfig /flushdns
```

## Verification

- `nslookup google.com` successfully returned DNS results.
- `ping google.com` successfully resolved the hostname and received replies.
- The DNS-related connectivity issue was resolved.

## Commands used

```cmd
ipconfig /all
ping 1.1.1.1
nslookup google.com
ipconfig /flushdns
ping google.com
```

## Evidence

### 1. Browser symptom
![Browser DNS failure](images/01-browser-dns-failure.png)

### 2. Network configuration
![IP configuration with bad DNS](images/02-ipconfig-bad-dns.png)

### 3. IP connectivity succeeds
![Ping public IP succeeds](images/03-ping-public-ip-success.png)

### 4. DNS lookup fails
![DNS lookup failure](images/04-nslookup-failure.png)

### 5. Correcting DNS configuration
![Set known-good DNS](images/07-set-known-good-dns.png)

### 6. Flush resolver cache
![Flush DNS cache](images/09-flush-dns-cache.png)

### 7. DNS resolution restored
![DNS lookup succeeds](images/10-nslookup-success.png)

### 8. Hostname connectivity verified
![Ping hostname succeeds](images/11-ping-hostname-success.png)

## Skills demonstrated

- Windows network troubleshooting
- TCP/IP connectivity testing
- DNS troubleshooting
- Command Prompt diagnostics
- Root-cause isolation
- Resolution verification
- Technical documentation
