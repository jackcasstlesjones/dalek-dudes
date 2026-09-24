# Cyber Essentials: to-do before submission

Do the update items in the few days before we submit, not earlier.

---

## Jack

### Your Arch laptop (ThinkPad)

- [ ] Run `sudo pacman -Syu` and reboot if the kernel updated.
- [ ] Update any AUR (Arch User Repository) packages you have installed.
- [ ] Update Firefox and Chrome to the latest version.
- [ ] Uninstall Zen browser if it is installed.
- [ ] Run `sudo ufw status` and check it says "active". If not, run `sudo ufw enable`.

### Your phone

- [ ] Install the latest OS (operating system) update.
- [ ] Check automatic updates are on.
- [ ] Check the screen lock uses a PIN of at least 6 digits (or a password), with Face ID or fingerprint as an extra.

### Your cloud accounts

- [ ] Check MFA (multi-factor authentication, e.g. an authenticator app or passkey) is switched on for every account you have on: Google Workspace, GitHub, Supabase, Netlify, Vercel, Cloudflare, Hetzner, Xero, Microsoft 365, Apple iCloud, Claude, Discord, LinkedIn.
- [ ] Log out and back in to each one to confirm you are actually asked for the second factor.

### Hetzner servers (all 3)

- [ ] Run `sudo apt update && sudo apt full-upgrade` and reboot if asked.
- [ ] Check automatic security updates are on: `cat /etc/apt/apt.conf.d/20auto-upgrades` should show both lines set to "1". If not, run `sudo dpkg-reconfigure -plow unattended-upgrades` and choose Yes.
- [ ] Run `sudo ufw status verbose` and check it says "active". If not, run `sudo ufw allow OpenSSH` first, then `sudo ufw enable`.
- [ ] Run `sudo sshd -T | grep -i passwordauthentication` and check it says "no". If not, set `PasswordAuthentication no` in `/etc/ssh/sshd_config` and run `sudo systemctl restart ssh`. Keep a second SSH (secure shell) session open while you test.

### Supabase

- [ ] Check every client project has the minimum password length set to 12 (Authentication > Sign In / Providers > Email).
- [ ] Check rate limits are on in every client project (Authentication > Rate Limits).

---

## Max

### Your Mac

- [ ] Update to the latest macOS (at least Tahoe 26.6) in System Settings > General > Software Update.
- [ ] In the same place, click the (i) next to Automatic Updates and switch on every option, including "Install Security Responses and system files".
- [ ] Turn on the firewall in System Settings > Network > Firewall.
- [ ] Install all App Store updates.
- [ ] Update Chrome (menu > Help > About Google Chrome) and Firefox (menu > Help > About Firefox) if installed.
- [ ] Update Word and Excel if installed (Help > Check for Updates).
- [ ] Uninstall Zen browser if it is installed.
- [ ] If Moonlock is installed, open it, install any updates and check real-time protection is on.

### Your phone

- [ ] Install the latest OS (operating system) update.
- [ ] Check automatic updates are on.
- [ ] Check the screen lock uses a PIN of at least 6 digits (or a password), with Face ID or fingerprint as an extra.

### Your cloud accounts

- [ ] Check MFA (multi-factor authentication, e.g. an authenticator app or passkey) is switched on for every account you have on: Google Workspace, GitHub, Supabase, Netlify, Vercel, Cloudflare, Hetzner, Xero, Microsoft 365, Apple iCloud, Claude, Discord, LinkedIn.
- [ ] Log out and back in to each one to confirm you are actually asked for the second factor.

### Proxmox host

- [ ] Run `apt update && apt dist-upgrade` (or use Updates in the Proxmox web interface) and reboot if the kernel updated.
- [ ] Turn on the Proxmox firewall at Datacenter > Firewall > Options. Before enabling, add rules allowing port 8006 (web interface) and port 22 (SSH) from your home network so you don't lock yourself out.
- [ ] Check the home router has no port forwards to the Proxmox host or forge.

### forge (Ubuntu virtual server on Proxmox)

- [ ] Run `sudo apt update && sudo apt full-upgrade` and reboot if asked.
- [ ] Check automatic security updates are on: `cat /etc/apt/apt.conf.d/20auto-upgrades` should show both lines set to "1". If not, run `sudo dpkg-reconfigure -plow unattended-upgrades` and choose Yes.
- [ ] Run `sudo ufw status verbose` and check it says "active". If not, run `sudo ufw allow OpenSSH` first, then `sudo ufw enable`.
- [ ] Run `sudo sshd -T | grep -i passwordauthentication` and check it says "no". If not, set `PasswordAuthentication no` in `/etc/ssh/sshd_config` and run `sudo systemctl restart ssh`. Keep a second SSH (secure shell) session open while you test.

### Solidtime

- [ ] In the Cloudflare Zero Trust dashboard, add Google Workspace as a login method (Settings > Authentication).
- [ ] Add Solidtime as a self-hosted application under Access > Applications, with a policy that only allows @runintandem.com emails.
- [ ] Open Solidtime in a private browser window and check you get the Cloudflare and Google login before Solidtime loads.
- [ ] Check Solidtime can't be reached any other way (no public IP address or open port).

---

## Jason

### Your Mac

- [ ] Update to the latest macOS (at least Tahoe 26.6) in System Settings > General > Software Update.
- [ ] In the same place, click the (i) next to Automatic Updates and switch on every option, including "Install Security Responses and system files".
- [ ] Turn on the firewall in System Settings > Network > Firewall.
- [ ] Install all App Store updates.
- [ ] Update Chrome (menu > Help > About Google Chrome) and Firefox (menu > Help > About Firefox) if installed.
- [ ] Update Word and Excel if installed (Help > Check for Updates).
- [ ] Uninstall Zen browser if it is installed.
- [ ] If Moonlock is installed, open it, install any updates and check real-time protection is on.

### Your phone

- [ ] Install the latest OS (operating system) update.
- [ ] Check automatic updates are on.
- [ ] Check the screen lock uses a PIN of at least 6 digits (or a password), with Face ID or fingerprint as an extra.

### Your cloud accounts

- [ ] Check MFA (multi-factor authentication, e.g. an authenticator app or passkey) is switched on for every Tandem-related account you have on: Google Workspace, GitHub, Supabase, Netlify, Vercel, Cloudflare, Hetzner, Xero, Microsoft 365, Apple iCloud, Claude, Discord, LinkedIn.
- [ ] Log out and back in to each one to confirm you are actually asked for the second factor.

---

## Jaz

### Your Fedora laptop (Framework)

- [ ] Run `sudo dnf upgrade --refresh` and reboot.
- [ ] If you use Flatpak apps, run `flatpak update`.
- [ ] Update Firefox and Chrome to the latest version if installed.
- [ ] Uninstall Zen browser if it is installed.
- [ ] Run `sudo firewall-cmd --state` and check it says "running". If not, run `sudo systemctl enable --now firewalld`.

### Your phone

- [ ] Install the latest OS (operating system) update.
- [ ] Check automatic updates are on.
- [ ] Check the screen lock uses a PIN of at least 6 digits (or a password), with Face ID or fingerprint as an extra.

### Your cloud accounts

- [ ] Check MFA (multi-factor authentication, e.g. an authenticator app or passkey) is switched on for every Tandem-related account you have on: Google Workspace, GitHub, Supabase, Netlify, Vercel, Cloudflare, Hetzner, Xero, Microsoft 365, Apple iCloud, Claude, Discord, LinkedIn.
- [ ] Log out and back in to each one to confirm you are actually asked for the second factor.
