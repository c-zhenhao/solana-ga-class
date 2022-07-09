https://www.notion.so/metacamp-community/Setup-Tools-and-Environment-for-Solana-9ec85f4fb15b4cfd9ab45880e2a227ba

# Setup Tools and Environment for Solana

Tools required and the links to install, you can skip those tools that you have installed. The links below should work for windows, mac(m1 and x64), and Linux.

- visual studio code (text editor) and rust-analyzer (vscode plugin)
  - [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
- node (runtime for javascript)

  - [https://nodejs.org/en/download/](https://nodejs.org/en/download/) (download LTS version, recommended)

- git (version control tool)

  - [https://git-scm.com/downloads](https://git-scm.com/downloads)

- rust and cargo (programming language for Solana program (smart contract) )

  - [https://doc.rust-lang.org/cargo/getting-started/installation.html](https://doc.rust-lang.org/cargo/getting-started/installation.html)

- anchor (programming framework to simplify development of Solana program)

  - [https://book.solmeet.dev/notes/intro-to-anchor#installation](https://book.solmeet.dev/notes/intro-to-anchor#installation)

- GitHub desktop (optional) (GUI to use git and link with github)

  - [https://desktop.github.com/](https://desktop.github.com/)

- https://solanabeach.io/

# all materials are copyright metacamp / OpenHaus

# additional materials followed:

https://dev.to/edge-and-node/the-complete-guide-to-full-stack-solana-development-with-react-anchor-rust-and-phantom-3291

https://dev.to/nickgarfield/how-to-install-solana-dev-tools-on-an-m1-mac-kfn

- in smart contracts,

- in programmes - they are stateless;

  - a bit similar to express endpoints, they take in data
  - everything in solana its called accounts ?

- Program is an on-chain smart contract
  - Stateless, no global variables
  - Contains logic
- Program ID is the address/account the program is stored in
- Data for programs is stored in Accounts

  - Account is actually a buffer
  - Can be thought of like a file in an OS
  - Includes metadata that tells the runtime who is allowed to access the data and how
  - Held in validator memory and pay "rent" to stay there (2 weeks)

  - uses the hashes from the previous block
  - has a limit (~10MB?)
  - Solana is designed to have small data sizes in order to be fast

- Program Data Separation - Counter App Example
  - Account contains value of the counter
  - Program contains logic

# Accounts

pub struct AccountInfo {
pub key: PubKey,
pub is_signer: bool,
pub is_writable: bool,
pub lamports: mut u64>>,
pub data: mut [u8]>>,
pub owner: Pubkey # usually refers to the
pub executable: bool, # if true its a smart contract, if false, its a data account
pub rent_epoch: epoch # time probably
}

#[account]

pub struct Bracket {
// bucket capacity
pub volume: u8,
// last player
pub last_player: PubKey,
}

- rust is a low level programme, so you need to manage the

- https://github.com/metacamp-so/last-to-ten
