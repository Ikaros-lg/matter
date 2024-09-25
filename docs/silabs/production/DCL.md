# Matter Distributed Compliance Ledger

## What is the DCL

## What are the DCL Roles

As mentioned above, the DCL has various roles in which you can interact with the database. The most notable roles are as follows:

## What is Stored in the DCL

Below are the DCL Schemas that can be stored in the DCL and who is responsible for writing the information:

| **Schema** | **Information** | **Who Adds** |
|------------|-----------------|--------------|
| Vendor Schema | Vendor Information including: VID, Name, Website URL | Vendor Account (Member) |
| Device Model | Product Information like VID, PID, Device Type Product Name, Commissioning Hints, link to User Manual | Vendor Account (Member) |
| Device Software Version Model | VID, PID, Software Version, release notes | Vendor Account (Member) |
| Device Software Compliance | Certification Status of a Model-Version (VID, PID, Software Version)  | CSA Certification Center Account |
| PAA | List of all approved PAA (Product Attestation Authorities) | Approved by Trustee Account (Members / CSA)  |

## Access DCL

The CSA offers two ways to access the DCL. You can access via a Web UI that can be found at [https://webui.dcl.csa-iot.org/](https://webui.dcl.csa-iot.org/), or you can install the latest version and use the CLI Client, [https://github.com/zigbee-alliance/distributed-compliance-ledger/releases](https://github.com/zigbee-alliance/distributed-compliance-ledger/releases). Note that the CLI Client is platform specific to either Linux or Mac OSX.

You will need to create an account with the DCL and wait for CSA approval. Once approved for Vendor level access, you can enter your vendor information and add product information. **Silicon Labs recommends that you create a DCL Account sometime before Matter Certification Process is complete.**

## Preparing for Matter Certification

To write a certifiable product to the DCL, you need an Approved Vendor account. You can do this by creating a DCL account and sending a request to the CSA. Once you are an approved vendor account holder, you can enter the following schemas: Vendor Schema, Device Model, and the Device Model-Version into the DCL. Once this information is in the DCL, you should notify the certification team via the Knack system. You **must have the required DCL Entries input before the CSA can input your Certification**. When your product gets officially certified and the Test House publishes the test certification status, the CSA Certification Center Account can write the Device Software Compliance. Once this is done, the CSA Trustee Account can enter the PAA information of the device to the DCL.

## Using the DCL in Commissioning to Verify Matter Devices

In Matter Commissioning, the PAA are root certificates and are used to sign PAI intermediate certificates. The Certification chain **must** start with a trusted root certificate. This is where the DCL comes in. The DCL stores the PAAs of Matter devices. Here, the Commissioner verifies the PAA of the desired Matter device attempting to join the network. The  [Matter Credentials](https://github.com/project-chip/connectedhomeip/tree/master/credentials) includes fetch-paa-certs-from-dcl.py which will pull the production PAA certs from the DCL and store them in the production/paa-root-certs which is an already trusted source, for the chip tool to look for PAAs during commissioning.
