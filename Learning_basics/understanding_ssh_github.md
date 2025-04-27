# Understanding SSH Authentication with GitHub  
*A learning log from confusion to clarity.*

---

## 🧠 Why I Started This

I wanted to push code to GitHub using SSH, but things didn’t go smoothly.  
Rather than just copy and paste commands from Stack Overflow, I decided to slow down and understand what was really happening — and why.

---

## 🔍 What Didn’t Work (at First)

Even after creating an SSH key and registering it on GitHub, I got this error:

```
git@github.com: Permission denied (publickey).
```

I knew something wasn’t connected right, but I didn’t know what.

---

## 🧩 The Questions I Asked

To move forward, I started asking:

- What exactly is ed25519?
- How does GitHub verify me without accessing my machine?
- What is a key fingerprint?
- What happens if I use the same key for multiple projects or companies?
- How does Git decide which key to use?
- Do I really need a config file?

---

## 🔐 Key Things I Learned

### 1. SSH Keys Are Asymmetric

- My computer keeps a **private key**
- GitHub keeps the **public key** I registered
- When I push, my computer signs a message with the private key
- GitHub verifies it using the public key

No passwords or manual authentication needed — just key math.

---

### 2. ed25519 Is an Algorithm, Not a Personal ID

- It’s a type of encryption algorithm, not something unique to me
- It’s short, fast, and secure — that’s why it’s used
- My key is unique because of randomness in generation, not because of "25519"

---

### 3. Why It Failed (and How to Fix It)

I had created a key called `id_ed25519_personal`,  
but Git (by default) looks for a file named `id_ed25519`.

Because I didn’t tell Git to use the new key, it failed to authenticate.

### ✅ Solution: Add a basic SSH config

```
Host github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_personal
  IdentitiesOnly yes
```

This config told Git: when connecting to GitHub, use the correct key.

---

### 4. When to Use Multiple Keys

- If one key gets exposed, others remain safe
- If working across orgs/clients, keys can be revoked or rotated independently
- It makes audits and cleanup easier later on

For personal use, a single key is fine. For work or client projects, separation helps.

---

## 🧭 Tools & Commands I Used

```bash
# Create SSH key
ssh-keygen -t ed25519 -C "your_email@example.com" -f ~/.ssh/id_ed25519_personal

# Check the public key
cat ~/.ssh/id_ed25519_personal.pub

# Test SSH connection
ssh -T git@github.com

# Set remote URL (if needed)
git remote set-url origin git@github.com:yourname/repo.git

# Git flow
git add .
git commit -m "First push using SSH"
git push origin main
```

---

## 💬 Final Thoughts

This wasn’t a deep dive into SSH internals,  
but I now understand how SSH authentication works, why it failed for me, and how to manage keys more thoughtfully.

For future projects, I’ll use what I learned here to avoid similar confusion — and help others do the same.
