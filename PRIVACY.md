# Privacy Policy for SandSync
**Last Updated:** 2026-02-21

This Privacy Policy explains how SandSync collects, uses, and protects your data. I believe in keeping your information as secure and anonymous as possible. I only collect the absolute minimum amount of data required to make the mod function, and I do not sell or share your data with anyone.

## Self-Hosted Databases
This Privacy Policy applies only to the official, premium SandSync database hosted by me, the developer. If you choose to host your own SandSync database using my GitHub setup guide, you are the sole Data Controller of that database, and this policy does not apply to you.

## 1. What Data I Collect
When you connect to the official SandSync database, I collect the following online identifiers and game data:

* **Minecraft UUIDs:** To identify you within your specific server or group and sync your gameplay stats.
* **Minecraft Usernames:** To display your stats on the leaderboard.
* **Email Addresses (For Group Owners Only):** If you are the Group Owner (the player who manages the subscription and invites others), I collect the email address associated with your Patreon account to verify your subscription status and allow you to recover your Group ID if lost.
* **Gameplay Statistics:** Raw in-game statistics (such as play time, jumps, blocks broken, etc.) necessary to generate the leaderboards.
* **Hashed Server Addresses:** A cryptographically hashed version of the server's identifier (like a server IP or domain) to ensure your stats are grouped into the correct server. I do not store the plain-text server address.

> **Note:** I do not collect your real name, physical address, IP address, private chat logs, or any other sensitive personal information.

## 2. How I Protect Your Data
I use advanced cryptographic techniques to ensure your data remains secure and anonymous. I never store your Minecraft UUID, Server Address, Email Address, or Group ID in plain text. Here is exactly how your data is protected:

* **Irreversible Hashing (Minecraft UUIDs, Email Addresses, Server Addresses, and Group IDs):** The moment this data reaches my database, it is passed through a one-way cryptographic hashing algorithm (SHA-256) combined with a secret, server-side key (a "pepper"). This scrambles the data into a random string. This process is irreversible; even if my database were compromised, no one could reveal your original UUID, Email, Server Address, or Group ID.
* **Encrypted Storage (Minecraft Usernames):** Usernames are securely encrypted using your specific Group ID as the key. My database only stores the scrambled ciphertext. Because the Group ID itself is never stored in plain text, a leaked database would be entirely useless to an attacker. Only players who hold the actual Group ID can decrypt the usernames, meaning attackers cannot read the leaderboards or see what servers you play on.
* **Raw Storage (Gameplay Statistics):** General in-game statistics (like play time or jumps) are stored in raw format to allow for fast querying and leaderboard generation. Because these statistics contain absolutely no personal identifiable information (PII) and are separated from your hashed identifiers, storing them raw poses no privacy risk.

## 3. How I Use Your Data
The data I collect is used exclusively for the following purposes:

* Syncing and displaying your Minecraft gameplay stats with other players in your specific server or group.
* Verifying subscription status for the Group Owner.
* Allowing the Group Owner to securely recover their Group ID if they lose it.

## 4. Data Retention and Deletion (Your GDPR Rights)
I believe in cleaning up after myself. SandSync has a strict data retention policy:

* **Automatic Deletion:** My database automatically purges any inactive groups and their associated player stats after 30 days of inactivity. If a subscription ends or your group stops playing, your data is completely and permanently erased automatically.
* **Manual Deletion (GDPR Article 11):** If you wish to have your data manually deleted before the 30-day purge, you must provide your Group ID along with your request. Because your data is highly encrypted and anonymized via cryptographic hashing, it is physically impossible for me to locate and delete your specific data without the Group ID to point me to the correct database row.

## 5. Third-Party Sharing
I do not sell, rent, or share any of your data with third parties, advertisers, or analytics companies. Your hashed data is stored securely using Supabase (my cloud database provider) solely for the purpose of keeping the mod online.

## 6. Contact
If you have any questions about this Privacy Policy, your data rights, or how your data is handled, please reach out to me via:
* My Discord: thesand_wastaken
