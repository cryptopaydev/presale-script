# Meme Coin Presale – Next-Gen Token Sale Solution
Welcome to the Meme Coin Presale project! This script delivers a robust, secure, and feature-rich token presale dApp, perfect for launching your meme coin or any crypto project with confidence and style.
## 🚀 About This Project
Meme Coin Presale is a powerful, plug-and-play React component designed to handle all aspects of a modern token presale. It supports seamless purchases with BNB and major stablecoins (BUSD, USDT, USDC), advanced referral tracking, and a beautiful, responsive UI. Built with security and flexibility in mind, it’s ready to supercharge your token launch!
## ✨ Features & Utilities
- **Multi-token Support:** Accepts BNB, BUSD, USDT, and USDC (BSC Mainnet & Testnet)
- **Secure Payment Flow:** Explicit approval required for stablecoins, with robust error handling
- **Referral Program:** Users earn a commission for every successful referral
- **Real-time Countdown:** Displays time left until presale ends
- **User Balances & Claim:** Shows purchased token balance and allows claiming after presale
- **Responsive Design:** Looks great on any device
- **Network Awareness:** Warns users if they are on the wrong chain
- **Instant Feedback:** Toast notifications for every action
- **Multiple Presale Stages:** Easily configure multi-stage presales, each with its own price and timer. The contract allows the owner to update stage prices and timing at any time.
- **Automatic Owner Payouts:** All purchased funds are sent directly to the owner's wallet as soon as a user buys.
- **Direct Referral Commissions:** Referral rewards are paid instantly and directly to the referrer’s wallet upon each successful purchase—no manual claiming required.
- **Flexible Timer Adjustments:** The contract supports multiple timers, so each stage can have its own countdown and end date, all adjustable by the owner.
## 💸 Payment Methods
- **BNB:** Users can buy tokens directly with BNB. The contract calculates the token amount based on the current BNB price.
- **Stablecoins (BUSD, USDT, USDC):** Users must first approve the presale contract to spend their tokens, then purchase. The dApp guides users through every step.
## 🤝 How Referral & Buy Functions Work
### Referral System
- Each user gets a unique referral link.
- When someone buys tokens using your link, you earn a commission (configurable in the contract).
- Referral stats and earnings are displayed in real-time.
- **Referral percentage is fully adjustable by the contract owner (up to a maximum of 10%).**
- **If you do not want to use the referral system, simply set the percentage to 0.**
- **To activate referrals, set the percentage to 5% or 10% (or any value up to 10%)—this can be changed at any time by the owner.**
- **Comprehensive Withdrawal Functions:** The contract provides secure withdrawal functions, allowing the owner to withdraw any structured tokens or payments held by the contract at any time. This includes support for structured payouts and multi-token withdrawals, giving the owner full control over contract-held funds.
### Buy Function
- **BNB:** Enter the amount, click Buy, confirm in wallet. Tokens are credited instantly.
- **Stablecoins:** Approve the contract, then Buy. The script ensures allowance and handles errors gracefully.
## 🛠️ Versions & Dependencies
- **Node.js:** v18+
- **React:** 18+
- **Vite:** ^4.0.0
- **Wagmi:** ^1.0.0 (Web3 React Hooks)
- **RainbowKit:** ^0.9.0 (Wallet UI)
- **Sonner:** ^1.0.0 (Toast notifications)
- **Viem:** ^2.0.0 (ETH data utils)
- **Tanstack React Query:** ^4.0.0
- **Tailwind CSS:** ^3.0.0
## ⚡ Integration – Add PresaleCard to Your React Project
1. **Copy the `/src/components/PresaleCard.tsx` and all dependencies from `/components`, `/hooks`, `/contracts`, `/contexts`, and `/config` into your project.**
2. **Install dependencies:**
   ```bash
   npm install wagmi @rainbow-me/rainbowkit viem sonner @tanstack/react-query tailwindcss
   ```
3. **Add `PresaleCard` to your app:**
   ```tsx
   import { PresaleCard } from './components/PresaleCard';
   // ...
   <PresaleCard />
   ```
4. **Configure your contract addresses in `/contracts/presale.ts`.**
5. **Style with Tailwind (already set up in this repo).**
## 🛠️ Setup & Installation
1. **Clone the repo:**
   ```bash
   git clone <your-repo-url>
   ```
2. **Install dependencies:**
   ```bash
   npm install
   ```
3. **Start the dev server:**
   ```bash
   npm run dev
   ```
4. **Open your browser at** `http://localhost:5173`
## 🎁 What This Script Offers
- Fast, secure, and modern presale dApp
- Multi-token support, referral system, and easy integration
- Full support and guidance for integration and customization
## 📄 Contract File Access & Security
- **Contract source code is NOT provided by default after purchase for security reasons.**
- **For audit, review, or integration, simply contact us via email—available 24/7.**
- **You will receive the contract .sol file free of charge after purchase by providing payment proof. This ensures safety and transparency for all buyers.**
## 📬 Contact & Support
**For contract files, integration help, or any questions, email:**
**cryptopay.dev@proton.me**  
_24/7 support for contract files, integration, and technical questions._
## 📝 Step-by-Step Integration & Support
1. **Contact us for contract files** (free, instant delivery)
2. **Integrate the PresaleCard as described above**
3. **Configure your addresses and environment**
4. **Deploy, test, and launch your presale with confidence!**
5. **Reach out anytime for support—we’re here to help you succeed!**
Unleash your meme coin’s full potential with the ultimate presale dApp. Fast setup, robust features, and world-class support—get started today!

## 🔑 WalletConnect Project ID & Contract Address Setup
To enable wallet connection, you need a WalletConnect Project ID. This is required for RainbowKit and Wagmi to function properly.
**How to get your WalletConnect Project ID:**
1. Go to https://cloud.walletconnect.com/
2. Sign up or log in with your email.
3. Create a new project.
4. Copy the Project ID from your project dashboard.
5. Replace the default `projectId` value in `src/config/wagmi.ts` with your own:
   ```ts
   projectId: "YOUR_WALLETCONNECT_PROJECT_ID"
   ```

**How to set contract and stablecoin addresses:**
- Open `src/contracts/presale.ts`.
- Replace the values in the `CONTRACT_ADDRESSES` object:
   ```ts
   export const CONTRACT_ADDRESSES = {
     PRESALE: "YOUR_PRESALE_CONTRACT_ADDRESS",
     BUSD: "YOUR_BUSD_ADDRESS",
     USDT: "YOUR_USDT_ADDRESS",
     USDC: "YOUR_USDC_ADDRESS",
     // ...
   }
   ```
- Make sure you use the correct addresses for your deployment network (mainnet or testnet).

After updating these values, your presale dApp will be fully connected to your contracts and ready for users to join!

**How to change the default chain (network):**
- Open `src/config/wagmi.ts`.
- Find the line: `export const defaultChain = bscTestnet;`
- To use BSC Mainnet, change it to: `export const defaultChain = bsc;`
- To use BSC Testnet, keep it as: `export const defaultChain = bscTestnet;`
- Make sure your contract and stablecoin addresses match the selected network.

This ensures your dApp defaults to the correct network for your deployment. Update the chain and addresses together for a seamless user experience!

**How to change the presale timer or end date:**
- Open `src/components/PresaleCard.tsx`.
- Find the line (near the top):
  ```ts
  const PRESALE_END_DATE = new Date('2025-12-31T23:59:59').getTime();
  ```
- Change the date string to your desired end date and time, e.g.:
  ```ts
  const PRESALE_END_DATE = new Date('2026-01-15T20:00:00').getTime();
  ```
- Save the file and restart your dev server if needed.
- For multi-stage presales, timers and stage end dates are managed via the smart contract (contact support for advanced configuration).

This allows you to easily control when the presale ends or adjust for new stages directly in the code or contract.

## 📜 Smart Contract Functions Overview
The presale smart contract is designed to be flexible, secure, and easy to manage. Here are the key functions available to the owner and users:

**Owner Functions:**
- `setStage(uint256 stage, uint256 price, uint256 endTime)`: Set or update the current presale stage, token price, and stage end time.
- `setReferralPercent(uint256 percent)`: Adjust the referral commission percentage (0–10%).
- `withdraw(address token, uint256 amount)`: Withdraw any ERC20 token or BNB from the contract to the owner’s wallet (supports multi-token and structured payouts).
- `enableClaim(bool status)`: Enable or disable claiming of purchased tokens.
- `setStablecoinAddress(address busd, address usdt, address usdc)`: Update stablecoin addresses if needed.

**User Functions:**
- `buyWithBNB(uint256 amount)`: Buy tokens directly with BNB.
- `buyWithStablecoin(address token, uint256 amount)`: Buy tokens with BUSD, USDT, or USDC after approval.
- `claim()`: Claim purchased tokens after claim is enabled.
- `getReferralLink(address user)`: Generate a unique referral link for each user.
- `referralStats(address user)`: View your referral stats and earnings.

All functions are designed for maximum security and transparency. For a full list of contract functions and details, request the contract file by email.
