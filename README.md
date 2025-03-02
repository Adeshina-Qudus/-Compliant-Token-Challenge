# Aleo Compliant Token

## Description
This Leo program, `compliant_token.aleo`, implements a token with KYC/AML enforcement and daily spending limits. Users must be KYC-verified to participate, ensuring regulatory compliance.

## Compliance Feature
- **KYC/AML Enforcement**:
  - `kyc_verified` mapping tracks verified users.
  - `issue_limit` and `transfer_private` enforce KYC status.
- **How It Works**: Only verified users can receive spend limits or transfer tokens (max 10B/day).
- **Use Case**: Regulated token system with privacy.

## Structure
- `src/main.leo`: Main program.
- `build/`: Custom folder with `program.json` and `imports/token_registry.aleo`.

## Deployment Instructions
1. **Prerequisites**:
   - Leo: `cargo install leo-lang`
   - Credits: `faucet.testnet3.aleo.network`.
2. **Setup**:
   - Clone: `git clone https://github.com/Adeshina-Qudus/-Compliant-Token-Challenge.git`
   - `cd aleo-compliant-token`
3. **Build**:
   - `leo build --network testnet --endpoint "https://api.testnet3.aleo.network"`
4. **Deploy**:
   - `leo deploy --network testnet --private-key <your_private_key> --endpoint "https://api.testnet3.aleo.network"`
   - Duration: ~30s-2min.
5. **Verify**: `explorer.testnet3.aleo.network`.
