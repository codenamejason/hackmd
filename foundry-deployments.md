# Allo - Hardhat vs Foundry Deployments

### Overview:

Hardhat and Foundry are two distinct frameworks used for developing and deploying smart contracts on the Ethereum blockchain. Here's an overview of some differences between Hardhat and Foundry deployments, particularly focusing on the handling of proxy upgradeable contracts:

1. **Deployment of Proxy Upgradeable Contracts**:
   - In Hardhat, the deployment of proxy upgradeable contracts seems to be more straightforward. An example provided on a Stack Exchange post shows the `upgrades.deployProxy` method being used for this purpose in Hardhat [[1](https://ethereum.stackexchange.com/questions/147931/how-to-deploy-a-upgradable-proxy-contract-in-mainnet-fork-using-foundry#:~:text=const%20ProxyC%20%3D%20await%20upgrades,share%20their%20knowledge%2C%20and)].
   - In contrast, the discussion did not provide a corresponding method for deploying proxy upgradeable contracts in Foundry, indicating it might not support this feature as seamlessly as Hardhat does.

2. **Configuration**:
   - Both frameworks use configuration files, with Hardhat utilizing a `hardhat.config.js` file, and Foundry generating a `foundry.toml` file upon project creation.
   - Hardhat allows for the addition of multiple networks in its configuration file which can be later used to deploy contracts. However, Foundry does not currently support this feature. In Foundry, most additional parameters you can add to the `foundry.toml` file are related to tests such as verbosity, account, balance, gas price, etc [[2](https://chainstack.com/foundry-hardhat-differences-performance/)].

3. **Usability & Complexity**:
   - Foundry is marketed as "the framework for pros" and includes more tools for sophisticated smart contract analysis. However, it's mentioned that this doesn't necessarily make it more professional software [[3]](https://jamesbachini.com/hardhat-vs-foundry/#:~:text=Usability%20%26%20Complexity%20Foundry%20is,is%20more%20professional%20software%20however).

4. **Templates**:
   - There's mention of a Hardhat-based and Foundry-based template for developing upgradeable Solidity smart contracts on GitHub. This could be beneficial for developers looking to work with upgradeable contracts on either framework.

5. **Project Structure**:
   - The directory structure for contract files, test files, output, and dependencies are defined in the configuration files for both frameworks, with slightly different default folders.

Foundry's apparent lack of support for deploying proxy upgradeable contracts as seamlessly as Hardhat—is consistent with the information sourced. This might necessitate additional steps or different methods to achieve a similar result when using Foundry.

Sources:
[[1]]()
[[2]](https://chainstack.com/foundry-hardhat-differences-performance/)
[[3]](https://jamesbachini.com/hardhat-vs-foundry/#:~:text=Usability%20%26%20Complexity%20Foundry%20is,is%20more%20professional%20software%20however)