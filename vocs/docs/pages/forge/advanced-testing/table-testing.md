BASE_RPC_URL="https://mainnet.base.org"
BASE_SEPOLIA_RPC_URL="https://sepolia.base.org"
source .env
cast wallet import deployer --interactive
forge create ./src/Counter.sol:Counter --rpc-url $BASE_SEPOLIA_RPC_URL --account deployer
