# describe

The **`describe`** command provides detailed information about the configurations of existing deployments in the Slot ecosystem, including Katana, Torii, and Madara services. It retrieves various configuration details, ensuring that users can view and verify the current settings of their deployments.


### Usage

```sh
slot deployments describe <Project Name> [service] [options]
```

### Parameters

- **`<Project Name>`** The name of the project associated with the deployment.
- **`[service]`** The specific service to update. Valid options are `Katana`, `Torii`, and `Madara`.

### Options


### General Options

- `--version <version>`
  - Specify the version of the service.

- `--tier <tier>`
  - Deployment tier, e.g., `basic`.

### Service-Specific Options

**Katana**:

- `--block-time <time>`
Set the block time for the deployment.

- `--fork-rpc-url <URL>`
   Specify the RPC URL to fork.

- `--fork-block-number <number>`
   Block number to fork from.

- `--disable-fee <boolean>`
   Enable or disable fee processing.

- `--gas-price <price>`
   Set the gas price.

- `--invoke-max-steps <steps>`
   Maximum steps for invoke operations.

- `--validate-max-steps <steps>`
   Maximum steps for validate operations.

**Torii**:

- `--world <world_id>`
   Identifier for the virtual world.

- `--start-block <block>`
   Start block for the deployment.

- `--index-pending <boolean>`
   Enable or disable indexing of pending transactions.

### Examples

1. **Describe a Katana Deployment:**
    
    ```sh
    slot deployments describe "MyProject" Katana --version "1.2"
    ```
    
2. **Describe a Torii Service Deployment:**
    
    ```sh
   slot deployments describe "MyProject" Torii --world 0x4fa481f41522b90b3684ecfab7650c259a76387fab9c380b7a959e3d4ac70f
    ```
