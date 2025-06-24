
# 🚀 Nexus Testnet III – Prover Node Setup Guide (Hindi 🇮🇳)

Namaste doston! 🙏  
Yahan aapko milenge simple steps Nexus zkVM Prover banne ke liye 💻🔐  
Aapke paas do tareeke hain contribute karne ke:

---

## 🌐 Method 1: Web Browser se Setup

1. Visit karo: [https://app.nexus.xyz/](https://app.nexus.xyz/) 🌐  
2. Apna **Wallet connect** karo 🔗  
3. **Email bhi add karo** (Wahi email use karo jo Testnet 1 & 2 mein kiya tha) 📧  
4. Done! Aap contribute kar rahe ho 🧠💪  

---

## 🖥️ Method 2: Linux Server Setup (CLI Users ke liye)

### 🔁 Step 0: Purane Users ke liye
```bash
rm -rf .nexus
```

---

### 📦 Step 1: Dependencies Install karo
```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y protobuf-compiler
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev -y
```

---

### 🦀 Step 2: Rust Install karo
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
# Install ke dauraan 'Enter' dabayein for default settings
source $HOME/.cargo/env
export PATH="$HOME/.cargo/bin:$PATH"
rustup target add riscv32i-unknown-none-elf
```

---

### ⚙️ Step 3: Correct Protobuf Version Install karo
```bash
sudo apt-get remove -y protobuf-compiler
wget https://github.com/protocolbuffers/protobuf/releases/download/v30.0-rc1/protoc-30.0-rc-1-linux-x86_64.zip
unzip protoc-30.0-rc-1-linux-x86_64.zip -d /usr/local/
sudo chmod +x /usr/local/bin/protoc
```

---

### 📺 Step 4: Screen Session Start karo
```bash
sudo apt install screen
screen -S nexus
```

---

### 🚀 Step 5: Nexus CLI Install & Start karo
```bash
sudo curl https://cli.nexus.xyz/ | sh
source ~/.bashrc
nexus-network start --node-id your-node-id
# ⚠️ Apna node-id yahan daalein (niche dekhein kaise milega)
```

---

## 🧾 Node ID kaise milega?

### ✅ Option 1: Web Dashboard se
1. Visit karo: [https://app.nexus.xyz](https://app.nexus.xyz)  
2. ➕ Add Node → **Add CLI Node**  
3. Copy karo apna **Node ID** aur upar ke step mein daalo  

---

### 💻 Option 2: CLI ke through
```bash
nexus-network register-user --wallet-address your-wallet-address
nexus-network register-node
nexus-network start
```

📁 Credentials save ho jaayenge: `~/.nexus/credentials.json`

🧹 Clear karne ke liye:
```bash
nexus-network logout
```

---

## 🧠 Screen Tips (Important for background run)

- Detach hone ke liye: `CTRL + A + D`  
- Wapas screen join karne ke liye: `screen -r nexus`

---

## 🎉 Ho gaya! Aapka node ready hai 💪🚀

Agar koi dikkat aaye, community hamesha help karne ke liye ready hai!

📢 Official Support:

- 🌐 Telegram Channel: [CryptoRikhav](https://t.me/CryptoRikhav)  
- 💬 TG Support Group: [Support Link](https://t.me/+ljjr6Gd6XSZiNzM9)

---

🛠️ Happy Proving & Keep Building! 🔐🧱  
⭐ Agar guide helpful lagi, to repo ko ⭐ zarur dena!
