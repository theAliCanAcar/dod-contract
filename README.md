# DoD Contract

Turn a task into an immutable definition of done with verifiable acceptance criteria.

Standalone ES module. No npm install required. Works in **Node.js 20+** and modern browsers (serve over HTTP for browser demos).

## Install / import

Copy the files into your project, or clone this repository:

```js
import { createContract } from './dod-contract.js';
const contract = createContract({id:'invoice', task:'Produce invoice total 42',
  criteria:[{id:'total',description:'JSON total equals 42'}]});
console.log(contract);
```

## Use cases

### 1. Turn a request into a testable brief

- **Scenario:** An agent is asked to generate an invoice.
- **Outcome:** Define the required total and output format before a builder starts.

### 2. Protect a migration’s acceptance criteria

- **Scenario:** Several agents share a database migration task.
- **Outcome:** Give each agent the same immutable requirements and explicit constraints.

## Exports

- `createContract`
- `mandatoryCriteria`

## Notes

- Keep API keys and secrets out of this module and out of browser storage.
- Treat verification callbacks, ledger writers, and permission checks as trusted application code.
- This library is intentional local reliability plumbing, not a claim of cryptographic attestation unless stated in the source comments.

## License

MIT
