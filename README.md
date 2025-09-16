webhook-controlled dashboard for pi >> TV display (non-interactive by design)

# Raspberry Pi Kiosk Display

This project turns a Raspberry Pi into a headless kiosk display for a TV or monitor. On boot, it launches Chromium in full-screen mode (Openbox session) and loads a default page (e.g. Frigate). A lightweight Flask webhook API allows switching the displayed page remotely, limited to homelab/local URLs and protected by an auth token.

The setup uses systemd services to manage both the browser and the webhook, with a path unit watching for URL changes. It’s designed to be simple, resilient, and secure for LAN/Tailscale use.