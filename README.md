# Blockful Challenge - Governance APP

## Overview

This challenge involves building a complete governance system with token delegation functionality. You'll work with smart contracts, frontend development, and blockchain indexing to create a comprehensive governance solution.

## Challenge Requirements

### 1. Governance Token Implementation

Create a governance token that supports delegation:

- Use `ERC20Votes` or `ERC721Votes` from OpenZeppelin
- Implement proper delegation mechanics
- Include permit functionality for gasless approvals
- Ensure the token can be used for voting power delegation\

The governance token should:

- [ ] Inherit from `ERC20`, `ERC20Permit`, and `ERC20Votes` (or 721)
- [ ] Implement required function overrides

### 2. Event Indexing with Ponder

Use Ponder to index delegation events:

- Create database schema
- Index relevant events around delegation
- Real-time updates when new delegations occur

Schema considerations:

- Delegation entities with delegator/delegatee relationships
- Historical delegation data
- Event timestamps and block numbers

> **_Bonus Points:_**
>
> - Implement delegate removal functionality

### 3. Frontend Application

Build a user interface for token delegation:

- Display token balance and voting power
- Allow users to delegate their tokens to other addresses
- Show delegation history and current delegations
- Responsive design for mobile and desktop

Key features:

- Transaction status feedback
- Error handling for failed transactions

> **_Bonus Points:_**
>
> - Add delegation historical chart
> - Real-time balance updates (relying on real time state management like [SWR](https://swr.vercel.app/), [react-query](https://tanstack.com/query/latest/docs/framework/react/overview))

## Project Structure

```tree
blockful-challenge-governor/
├── apps/
│   ├── contracts/          # Smart contracts (Foundry)
│   │   ├── src/
│   │   │   └── GovToken.sol
│   │   ├── script/
│   │   └── tests/
│   ├── frontend/           # Next.js frontend
│   │   ├── src/
│   │   │   └── app/
│   │   └── public/
│   └── indexer/            # Ponder indexer
│       ├── src/
│       ├── abis/
│       └── ponder.config.ts
├── package.json
└── pnpm-workspace.yaml
```

## Getting Started

### Prerequisites

- Node.js 18+
- pnpm
- Foundry (for smart contracts)

### Installation

1. Clone the repository
2. Install dependencies:

```bash
pnpm install
```

3. Set up environment variables:

```bash
PRIVATE_KEY=your_private_key
RPC_URL=your_rpc_url
```

## Evaluation Criteria

1. **Smart Contract Quality**
   - Proper implementation of ERC20Votes
   - Security best practices
   - Gas optimization
   - Comprehensive tests

2. **Indexing Implementation**
   - Accurate event indexing
   - Efficient data storage
   - API performance
   - Data consistency

3. **Frontend User Experience**
   - Intuitive delegation interface
   - Responsive design
   - Error handling
   - Real-time updates

4. **Code Quality**
   - Clean, readable code
   - Proper documentation
   - TypeScript usage
   - Error handling

## Submission

1. Complete the implementation according to requirements
2. Ensure all tests pass
3. Document any assumptions or design decisions
4. Provide deployment instructions
5. Include a brief demo video or screenshots

## Resources

- [OpenZeppelin ERC20Votes](https://docs.openzeppelin.com/contracts/4.x/api/token/erc20#ERC20Votes)
- [Ponder Documentation](https://ponder.sh/docs)
- [Foundry Book](https://book.getfoundry.sh/)
- [Next.js Documentation](https://nextjs.org/docs)

## Support

If you have questions about the challenge requirements, please reach out to the Blockful team.

Good luck! 🚀
