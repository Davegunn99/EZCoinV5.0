### **Release Notes for EZCoin v5.1.0**

---

#### **EZCoin Core v5.1.0 (Major Update)**
This release introduces significant changes to the EZCoin (EZC) blockchain, ensuring the sustainability and security of the network. It is a mandatory upgrade for all wallet users, node operators, and miners to remain compatible with the updated blockchain rules.

---

### **Key Changes in v5.1.0**

1. **Revised Block Reward Structure:**
   - **Previous Structure:**
     - Block reward was fixed at **100 EZC per block** until reaching the maximum supply of **1 billion EZC** at block height **8,670,001**.
     - After this, the block reward would become 0, effectively ending mining rewards.
   - **Updated Structure:**
     - Block reward will remain at **100 EZC per block** until block height **2,061,199**.
     - Starting at block height **2,061,200 (inclusive)**, the block reward will decrease to **1 EZC per block**.
     - This reduced block reward will continue until block height **662,941,400**.
     - After block height **662,941,400**, the block reward will become **0**, as the total supply cap of **1 billion EZC** will be reached.

   **Advantages of the New Reward Structure:**
   - **Longevity of Mining:** Extends the mining process by reducing the rate at which new coins are introduced.
   - **Network Security:** Ensures consistent miner participation and maintains blockchain stability for a much longer duration.
   - **Sustainability:** Aligns with the project's goal of a sustainable and thriving network for years to come.

2. **Checkpoints Added:**
   - New **checkpoints** have been implemented to secure the network and provide additional protection against long-range attacks.
   - These checkpoints ensure that nodes can quickly verify the blockchain's validity and reject invalid chains, improving network robustness.

---

### **Upgrade Instructions**

#### **Before You Start**
1. **Backup Your Wallet:**
   - Make a secure backup of your `wallet.dat` file, as it contains your private keys.
   - Backup locations:
     - **Windows:** `C:\Users\<YourUsername>\AppData\Roaming\EZCoinV5`
     - **Linux:** `~/.ezcoinv5`
     - **macOS:** `~/Library/Application Support/EZCoinV5`

2. **Ensure No Wallet Instances are Running:**
   - Close any running instances of the EZCoin wallet to avoid conflicts during the upgrade.

#### **Upgrade Steps**
1. **Download the Latest EZCoin Wallet:**
   - Visit the [official EZCoin website](https://myezcoin.com) or the [GitHub repository](https://github.com/Davegunn99/EZCoinV5.0/releases/latest) to download the updated wallet v5.1.0.
   - Select the appropriate version for your operating system (Windows, Linux, macOS).

2. **Replace Wallet Binaries:**
   - Locate your wallet installation folder:
     - **Windows:** `C:\Program Files\EZCoinV5`
     - **Linux:** `/usr/local/bin`
     - **macOS:** `/Applications/EZCoin V5.app`
   - Replace the existing binaries (`ezcoind`, `ezcoin-qt`, etc.) with the new ones from v5.1.0.

3. **Restart Your Wallet:**
   - Launch the updated wallet. It will automatically apply the new block reward and checkpoints.

4. **Verify the Upgrade:**
   - Check the wallet version:
     - In the GUI: Navigate to `Help > About EZCoin`.
     - In the CLI: Run the following command:
       ```bash
       ezcoin-cli getinfo
       ```
     - Confirm that the `"version"` field displays `5010000`.

---

### **For Miners**
- **Block Reward Changes:**
  - The updated reward of **1 EZC per block** will take effect at block height **2,061,200**.
  - Ensure your mining software is compatible with the updated blockchain rules.
- Miners on older wallet versions will not be able to submit valid blocks after block height **2,061,199**.

---

### **Common Issues and Troubleshooting**
1. **Wallet Not Syncing:**
   - Ensure your wallet is updated to v5.1.0.
   - If syncing issues persist, add these nodes to your `ezcoin.conf` file:
     ```
     addnode=seed1.myezcoin.com
     addnode=seed2.myezcoin.com
     addnode=seed3.myezcoin.com
     addnode=seed4.myezcoin.com
     ```

2. **Block Reward Still Showing 100 EZC:**
   - This may occur if you are running an older wallet version or have not synced past block height **2,061,200**.

3. **Reindexing Issues:**
   - If required, use the following command to reindex:
     ```bash
     ezcoin-cli -reindex
     ```

4. **Need Help?**
   - Visit the [EZCoin Support Page](https://ezcoincryptocurrency.com/contact-us).
   - Join the community on [Telegram](https://t.me/ezcoincrypto) or [Discord](https://discord.gg/jQsvTpCpwu) for assistance.

---

### **Summary**
This update to v5.1.0 is a critical step for EZCoin's long-term sustainability and network security. By revising the block reward structure and introducing checkpoints, EZCoin ensures a robust and thriving ecosystem for all participants. Upgrade now to stay compatible and enjoy the benefits of a sustainable blockchain!