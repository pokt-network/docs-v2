# Onboarding New Voters

Below are the steps for onboarding to the new system.&#x20;

## New Citizens

Enter the Discord channel <mark style="color:red;">\[Name]</mark> where you will complete the quests using [Wonderverse](https://wonderverse.com/).&#x20;

First, Complete the Onboarding Quest. You must follow the steps to set up and verify a Gitcoin Passport, a mygateway.xyz Username, and the Eth/EVM Voter Wallet that you intend to use.

These 3 pieces of information are essential to be DAO voters.  A simple example video for each is included here:

* [Passport Loom Video](https://www.loom.com/share/b21febf6a41b41ae95cd5305a1441059)&#x20;
* [Gateway.xyz Loom](https://www.loom.com/share/18cfeba0a355433ebf7080e189de4b82)&#x20;
* Wonderverse Loom Video
  * **DNA Quest**: This is half of what is required to become a POKT Citizen
  * **DAO Quest:** This is the second half of what is required to become a DAO Citizen

Upon successful completion of these three steps, you will receive a link to claim your POKT Citizenship. After completing this step, you can view your Citizenship in[ mygateway.xyz](http://mygateway.xyz) under “Data Assets”

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

As a Citizen, the impact you create through the DAO’s contribution mechanisms will earn you a vote in the DAO. Keep in mind, without Citizenship the system will not account for any of your other badges and your vote will be set to zero.

## Genesis Voters <a href="#docs-internal-guid-17c8b37e-7fff-5f8e-ba81-63307b63dad2" id="docs-internal-guid-17c8b37e-7fff-5f8e-ba81-63307b63dad2"></a>

In addition to our existing voters, many community members will become eligible voters upon completing the Citizenship requirements. This is because they have previously created an impact via the DAO contribution mechanisms (since the start of 2023). We are calling this group “Genesis Voters”.

The people included in this list will become Genesis Voters upon completing the [citizenship requirements](onboarding-new-voters.md#new-citizens):[ Genesis Voters List](https://docs.google.com/spreadsheets/d/1bd0LhJlbcY7HdotaZdu\_675XThZTx2nmgsUmpTPmpEs/edit#gid=0)

Genesis voters should contact Ben or Mehrdad upon creating their mygateway.xyz username so we can verify and issue their credentials. Please confirm with us via Discord.

## Stakers <a href="#docs-internal-guid-e5d3a62f-7fff-a536-109a-3878e1b358d5" id="docs-internal-guid-e5d3a62f-7fff-a536-109a-3878e1b358d5"></a>

The new system provides voting power to productive capital staked in the network. If you wish to claim Staker power please follow the steps below:

### Custodial Service Providers

As a custodian, you can vote with all of the POKT staked in your custodial nodes. This is enabled by connecting these nodes to a single credential via your service domain. You need to:

1. Navigate to the cloud provider where you have set up your service domain (Cloudflare, GoDaddy, etc.)
2. Once you have logged in, find your domain and add a new record with the txt type for the main domain (even if you’re using subdomains, the record must be created under the main domain). [Here’s an example of how to add a txt record to Cloudflare.](https://www.youtube.com/watch?v=K1B5UwSBwko)
3.  &#x20;In the newly added txt record, add the following text `POKT_GATEWAY_ID=your-gateway- username` and replace “your-gateway-username” with your own mygateway.xyz username. For example, if we consider the screenshot below owner of the POKTscan.cloud custodian. This person has to add a txt record containing `POKT_GATEWAY_ID=mytestaccount1` to their DNS records. &#x20;

    <figure><img src="https://lh7-us.googleusercontent.com/535YHfKVSCezu6PDEfwDZyKxSmZ4CuE4mv4g027a7xmMW7oVmOCJeO7T6ydY2M5CmTy5pev-9BZafmp2YpU1pl7pv6L5JpOIQRsaVDzz3E3OL7_ww7-VcwdDNnc_Orw-LNfySwxVHwvQi0ACEOeWNPg" alt=""><figcaption></figcaption></figure>
4. Save, and your work is completed. Your PDA will be generated automatically within the next 24 hours.
5.  To double-check and make sure you have done the steps correctly you can use [DNSchecker.org](https://dnschecker.org)

    <figure><img src="../../../.gitbook/assets/Screenshot 2024-03-26 at 12.48.21 PM.png" alt=""><figcaption></figcaption></figure>

You can retake the same steps if you control multiple service domains.

### Non-Custodial Stakers (Users) <a href="#docs-internal-guid-78ff420c-7fff-6007-28e8-bcbdc255c20c" id="docs-internal-guid-78ff420c-7fff-6007-28e8-bcbdc255c20c"></a>

Regular stakers must go through the following steps to claim their staker credentials.

1. Navigate to[ mygateway.xyz](http://mygateway.xyz) dashboard and log into your account.
2.  Once you have logged in to your account, at the bottom left click on your Gateway username and then click on `Manage Gateway ID`

    <figure><img src="https://lh7-us.googleusercontent.com/q9UWaEYMGt6tRITe8xDJIt3pxgY9f-EvjefhsaX5cralWcIBSfJWCjq5fxIXVRC35iuISXjKcv7gWP4zokwYGUkkUJ4YrfN9VrPjUGB_l14uyEShZ_lQ_Rra4ZwcdLWtTc7cfXzMqTenBVSYzlihATo" alt=""><figcaption></figcaption></figure>

    <figure><img src="https://lh7-us.googleusercontent.com/zvU6v8nNtKwicl91q2HUqsqg-xWDgJCbxCQnCwZenJfzarRP9-acxT3dYH70pscBgSG_7Uau5e8KW00rmSR08rAGnUIanSpitOliWOoR_cFkrPjTScqSSFOPHMzAKxnowkc3kYQPBZAG2t6uCVk8UAs" alt=""><figcaption></figcaption></figure>
3.  Scroll down and click on `+ Add Wallet`

    <figure><img src="https://lh7-us.googleusercontent.com/dBOjaSN-hcUnl74plAGiXFGRnkv885bbP9XJuxFtIsPDiBWpdXFlVMTdFb5vJSFamhJh3wxX2zFEddcfy_vw49kRpbTIlvPGgsTCXPLlkwYDiQ0M_vKLRyUNMjgSbu7SH-54-2p_XgcM8KQ0vmBLwf0" alt=""><figcaption><p> </p></figcaption></figure>
4.  Connect your POKT wallet. **Please keep in mind** that this is currently only supported via Node Wallet which you can download from[ here](https://chromewebstore.google.com/detail/nodewallet/ilibmadejjooogcniiomgdgbojkmlbim) and import your keyfile. The wallet that you have to connect is the output address of your node. If this output wallet is being used for more than one node, the system will automatically consider all of the connected nodes and calculate your total stake.&#x20;

    <figure><img src="https://lh7-us.googleusercontent.com/dmCMpIbk4jiduPyAiKKQgnO4NNfIZH8DDSwyKhpl_B3RfspydmLF2rjCf5cy2SHBFTM-70FWsCyQ-HoJnpyOjMQ5JE8JEqQqsEiirQ6cY13PUrlEj0Q_4snt7eXsDnFHdCvT6KqmIshcTLAQFSSgPz8" alt=""><figcaption></figcaption></figure>
5. After the previous step, your job is done. Your PDA will be issued automatically within the next 24 hours.

If you use more than one address as an output address for your nodes, you should connect all of them using the above steps.&#x20;
