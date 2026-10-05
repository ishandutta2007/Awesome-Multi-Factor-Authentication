# Awesome-Multi-Factor-Authentication

# Awesome-Multi-Factor-Authentication

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on TOTP Apps, Hardware Tokens, Self-Hosted Identity Providers & Enterprise MFA*
**Last updated: October 2026**

This repository tracks notable **commercial MFA platforms** and **open-source projects** for **Multi-Factor Authentication**. These tools help individuals and organizations add a second layer of security—TOTP codes, hardware keys, push notifications, or biometrics—on top of passwords.

**Examples** include Microsoft Authenticator, Google Authenticator, Duo Security, Authy, Yubico Authenticator, 1Password, LastPass Authenticator, Okta Verify, RSA SecurID, and PingID (the category leaders).

**Open-source emphasis**: The open-source MFA ecosystem is **exceptionally mature and production-proven**. **Aegis Authenticator** leads the privacy-focused Android tier with encrypted offline storage and no cloud dependency . **Ente Auth** and **Proton Authenticator** provide end-to-end encrypted cloud sync without vendor lock-in . **privacyIDEA** and **Keycloak** deliver enterprise-grade MFA management with TOTP, WebAuthn, FIDO2, and push tokens . **Authelia** offers lightweight 2FA/SSO for reverse proxies with a sub-20 MB container . This section documents these production-grade solutions.

## 📖 Table of Contents

- [☁️ SaaS/Hosted Platforms](#-saas-hosted-platforms)
- [🔓 Open-Source GitHub Projects](#-open-source-github-projects)
- [🤝 How to Contribute](#how-to-contribute)
- [⚠️ Disclaimer](#-disclaimer)

## ☁️ SaaS/Hosted Platforms

> **📊 Market Context**: The global MFA market is estimated at **~$15B in 2026**, growing toward **~$35B by 2032**. The sector is **moderately fragmented** — **Microsoft Authenticator** and **Google Authenticator** dominate consumer adoption through ecosystem bundling, while **Duo**, **Okta Verify**, and **RSA SecurID** lead enterprise deployments. **Critical security caveat**: **Google Authenticator's cloud backup lacks end-to-end encryption** — backed-up codes are potentially accessible to Google, and E2EE is still "planned for future implementation" as of late 2024 . **Authy's backup password cannot be recovered** — zero-knowledge architecture means forgotten passwords permanently lock users out of synced tokens . **Pricing varies dramatically**: consumer apps (Microsoft, Google, Authy, Yubico) are **free** , while enterprise platforms (Duo, Okta, RSA) require **custom quotes** starting at **$3/user/month** for Duo Essentials . No single vendor holds a winner-take-all position.

| Platform | Description | Pricing (Starting Tier) | Free Tier Limits | Company Size |
|----------|-------------|------------------------|------------------|--------------|
| **[Microsoft Authenticator](https://www.microsoft.com/en-us/security/mobile-authenticator-app)** | **Microsoft's free MFA app.** TOTP codes, push notifications, and passwordless sign-in for Microsoft accounts. | **Free** — no paid tier. | **Unlimited** — free with Microsoft account. | **~$281B revenue (Microsoft FY2025)** |
| **[Google Authenticator](https://support.google.com/accounts/answer/1066447)** | **Google's TOTP app.** Cloud backup introduced in 2023, syncing codes across devices via Google Account. **Lacks end-to-end encryption** . | **Free** — no paid tier. | **Unlimited** — free with Google account. **Cloud backup lacks E2EE** . | **~$350B revenue (Alphabet FY2025)** |
| **[Duo Security](https://duo.com/)** | **Cisco's MFA platform.** Push notifications, TOTP, WebAuthn, and hardware tokens for enterprise. | **Essentials**: **$3/user/month** (annual). **Professional**: **$6/user/month**. **Enterprise**: Custom . | **Free trial** available. **No perpetual free tier** for enterprise. | **Part of Cisco (~$63B revenue)** |
| **[Authy](https://authy.com/)** | **Twilio's MFA app.** Encrypted cloud backup with multi-device sync. **Backup password cannot be recovered** . | **Free** — no paid tier. | **Unlimited** — free with Authy account. **Backup password is irreversible** . | **Part of Twilio (~$4.9B revenue)** |
| **[Yubico Authenticator](https://www.yubico.com/products/yubico-authenticator/)** | **Hardware-backed TOTP app.** Stores secrets on YubiKey hardware, requiring physical key for code generation. | **Free** app; **YubiKey** hardware from **$50** . | **Unlimited** — free with YubiKey purchase. | **Private (~$500M+ revenue est.)** |
| **[1Password](https://1password.com/)** | **Password manager with built-in TOTP.** Stores 2FA codes alongside passwords, protected by master password. **Uses E2EE** . | **Personal**: **$2.99/month**. **Families**: **$4.99/month**. | **14-day free trial** . **No perpetual free tier**. | **Private (~$6.8B valuation est.)** |
| **[LastPass Authenticator](https://lastpass.com/)** | **LastPass's MFA app.** TOTP codes, push notifications, and backup. | **Free** with LastPass account . | **Unlimited** — free with LastPass. | **Part of LogMeIn** |
| **[Okta Verify](https://www.okta.com/)** | **Okta's MFA app.** Push, TOTP, and FastPass methods for enterprise identity. | **Bundled with Okta** subscriptions. | **Free trial** available. **No perpetual free tier**. | **~$2.5B revenue (Okta FY2025)** |
| **[RSA SecurID](https://www.rsa.com/)** | **Enterprise MFA pioneer.** Hardware tokens, software tokens, and push authentication. | **Custom enterprise pricing** — quote required. | **No free tier**. **Demo** required. | **Private (RSA)** |
| **[PingID](https://www.pingidentity.com/)** | **Ping Identity's MFA platform.** Push, TOTP, and biometric authentication for enterprise. | **Custom enterprise pricing** — quote required. | **No free tier**. **Demo** required. | **Private (~$500M+ revenue est.)** |

## 🔓 Open-Source GitHub Projects

| Repo | Description | Stars |
|------|-------------|-------|
| **[Aegis Authenticator](https://github.com/beemdevelopment/Aegis)** — **The gold standard for privacy-focused Android 2FA.** **Encrypted offline vault** — codes never leave your device . **Password or biometric lock** for app access. **Encrypted export/import** for device migration. **No cloud sync, no tracking, no ads** . Supports **TOTP and HOTP**. **GPL-3.0**. | [![Stars](https://img.shields.io/github/stars/beemdevelopment/Aegis?style=social&color=white)](https://github.com/beemdevelopment/Aegis/stargazers) | ~10,000 |
| **[Ente Auth](https://github.com/ente-io/ente)** — **E2E encrypted 2FA with optional cloud sync.** **End-to-end encrypted backups** — only you can decrypt your tokens . **Security audited by Cure53** . Shows **current and next code** simultaneously for seamless login. **Available on Android, iOS, macOS, Windows, and Web** . **No account required** for local use. **AGPL-3.0**. | [![Stars](https://img.shields.io/github/stars/ente-io/ente?style=social&color=white)](https://github.com/ente-io/ente/stargazers) | ~15,000 |
| **[Proton Authenticator](https://github.com/ProtonMail/proton-authenticator)** — **Proton's open-source 2FA app.** **E2E encrypted cloud sync** via Proton account . **Biometric/code lock** for local access. **Works fully offline** if no sync desired. **Bulk import/export** and QR code migration from other apps . Supports **TOTP, Steam, SHA1/256/512, custom code lengths** . **GPL-3.0**. | [![Stars](https://img.shields.io/github/stars/ProtonMail/proton-authenticator?style=social&color=white)](https://github.com/ProtonMail/proton-authenticator/stargazers) | ~2,000 |
| **[2FAS](https://github.com/twofas/2fas-android)** — **Open-source 2FA with 6M+ downloads.** **Optional encrypted backup** via Google Drive or proprietary backend . **No account required** . **Browser extensions** for Chrome, Firefox, Edge, and Safari. **Clean UI** with search, groups, and color coding . **Apache-2.0**. | [![Stars](https://img.shields.io/github/stars/twofas/2fas-android?style=social&color=white)](https://github.com/twofas/2fas-android/stargazers) | ~3,000 |
| **[FreeOTP](https://github.com/freeotp/freeotp-android)** — **Red Hat's lightweight TOTP/HOTP app.** **Minimalist, no-frills design** — ~2-3 MB storage . **No cloud sync, no backup** . Supports **TOTP and HOTP** with customizable algorithm, code length, and period . **Apache-2.0**. | [![Stars](https://img.shields.io/github/stars/freeotp/freeotp-android?style=social&color=white)](https://github.com/freeotp/freeotp-android/stargazers) | ~5,000 |
| **[privacyIDEA](https://github.com/privacyidea/privacyidea)** — **Enterprise-grade MFA management system.** Manages **TOTP, HOTP, OCRA, mOTP, YubiKey, FIDO U2F, FIDO2/WebAuthn, push, SMS, email, and SSH keys** centrally . Exposes factors via API consumed by **Keycloak, FreeIPA, NGINX, Gluu** . **v3.13** adds offline passkey registration on Windows/Linux . **AGPL-3.0**. | [![Stars](https://img.shields.io/github/stars/privacyidea/privacyidea?style=social&color=white)](https://github.com/privacyidea/privacyidea/stargazers) | ~3,500 |
| **[Keycloak](https://github.com/keycloak/keycloak)** — **The most widely deployed open-source IAM.** Covers **SSO, identity brokering, social login, and RBAC** . Native **SAML, OAuth2, OIDC, LDAP** support. MFA methods include **TOTP, WebAuthn, SMS, OIDC, email, push, biometric** . **Apache-2.0**. | [![Stars](https://img.shields.io/github/stars/keycloak/keycloak?style=social&color=white)](https://github.com/keycloak/keycloak/stargazers) | ~28,000 |
| **[Authelia](https://github.com/authelia/authelia)** — **Lightweight 2FA/SSO for reverse proxies.** **Sub-20 MB container, ~30 MB RAM** . **FIDO2 WebAuthn, TOTP, Duo push, passkeys** . **OIDC certified** . **YAML-configured** for version control . No multi-tenancy or PAM support . **Apache-2.0**. | [![Stars](https://img.shields.io/github/stars/authelia/authelia?style=social&color=white)](https://github.com/authelia/authelia/stargazers) | ~23,000 |
| **[Authentik](https://github.com/goauthentik/authentik)** — **Self-hosted IAM with SSO, LDAP, OAuth2/OIDC, SAML, SCIM** . **2025.12** adds **endpoint device management** for Windows/macOS/Linux, **WebAuthn Conditional UI**, and **multi-parent RBAC groups** . **2026.2** adds **Linux PAM support** for local device login . **AGPL-3.0**. | [![Stars](https://img.shields.io/github/stars/goauthentik/authentik?style=social&color=white)](https://github.com/goauthentik/authentik/stargazers) | ~14,000 |
| **[Rauthy](https://github.com/sebadob/rauthy)** — **Lightweight OIDC provider and SSO.** **WebAuthn/FIDO2/passkeys, TOTP, social login** . **Single binary or container** with low resource consumption . **v0.27** adds **rauthy-pam-nss** module for **Linux PAM/NSS integration** — local workstation login via YubiKey passkeys and MFA-secured SSH . No RADIUS or built-in LDAP server . **Apache-2.0**. | [![Stars](https://img.shields.io/github/stars/sebadob/rauthy?style=social&color=white)](https://github.com/sebadob/rauthy/stargazers) | ~1,500 |

**Additional open-source options worth exploring:**

| Repo | Description |
|------|-------------|
| **[andOTP](https://github.com/andOTP/andOTP)** — Android-only TOTP/HOTP app with encrypted backups, tags, panic button, and extensive customization. **MIT** . |
| **[Kanidm](https://github.com/kanidm/kanidm)** — Modern identity management platform with **pam_kanidm module** for Linux PAM and WebAuthn support. **MPL-2.0** . |
| **[FreeIPA](https://github.com/freeipa/freeipa)** — Linux identity management bundling LDAP (389-ds), Kerberos, DNS, and CA. Supports **TOTP, OTP, and FIDO2/passkey** . **GPL-3.0** . |
| **[LLDAP](https://github.com/nitnelave/lldap)** — Lightweight LDAP server with web UI. **No OAuth2/OIDC** — pairs with Keycloak or Authelia for full MFA. **GPL-3.0** . |
| **[SoloKey](https://github.com/solokeys/solo)** — Open-source hardware security key. YubiKey alternative with FIDO2 and U2F support . |
| **[Nitrokey](https://github.com/Nitrokey/nitrokey-3-firmware)** — Open-source hardware token with firmware that can be independently audited . |

## 🤝 How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## ⚠️ Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- MFA platforms handle sensitive authentication secrets; ensure proper encryption, backup strategies, and compliance with organizational security policies.
- **Critical security caveats**: **Google Authenticator's cloud backup lacks end-to-end encryption** — codes are potentially accessible to Google, and E2EE remains "planned for future implementation" as of late 2024 . **Authy's backup password cannot be recovered** — zero-knowledge architecture means a forgotten password permanently locks users out of synced tokens, requiring manual account recovery for every service . **FreeOTP has no backup feature** — losing your phone means losing access to all codes unless you saved secret keys manually .
- **Open-source reality**: The open-source ecosystem for MFA is **exceptionally mature and production-proven**. **Aegis Authenticator** is the gold standard for privacy-focused offline Android 2FA with encrypted storage . **Ente Auth** and **Proton Authenticator** provide E2E encrypted cloud sync without vendor lock-in . **privacyIDEA** and **Keycloak** deliver enterprise-grade MFA management with TOTP, WebAuthn, FIDO2, and push tokens . **Authelia** offers lightweight 2FA/SSO for reverse proxies with a sub-20 MB container . However, **commercial platforms** (Duo, Okta Verify, RSA SecurID) provide **managed infrastructure, enterprise SLAs, and dedicated support** that open-source alternatives require significant operational investment to match. The open-source path is **genuinely viable** for organizations and individuals seeking full data sovereignty and no subscription fees.

---

**Made for security engineers, IT administrators, privacy advocates, and anyone who wants better account security.**
Let's make multi-factor authentication more open, transparent, and secure.
