# **Step by step on how to integrate a new payment gateway into the VTEX platform**

</p>VTEX has a public contract (Payment Provider Protocol) for those who want to integrate its payment providers into the company's platform, the VTEX SmartCheckout system. This protocol enables providers to create a payment connector that interacts with VTEX's Gateway, that has its own PCI certification (so all payments are protected). 
Besides developing the connector, providers also need to test them and make sure they follow the required security standards before they can be available to the stores. 

<br>Below there are the steps you usually need to follow to implement an integration:

1. If your integration supports credit, debit or co-branded cards, before start developing, you have to assure that your payment connector follows one of these conditions:
- The connector is hosted in a secure environment that follows the PCI - DSS security standards. An Attestation of Compliance (AOC) is required in this case.
- The connector is developed by using Secure Proxy, where it receives tokens instead of sensitive data related to the card transaction, and the Gateway acts as a proxy to communicate with the acquirer.
2. Implement your payment connector according to our Payment Provider Protocol. This includes all the required endpoints. All the payment methods supported by your integration will have to be listed in the response of the List Payment Provider Manifest endpoint. Also, for each payment method, you will have to implement a specific behavior for the Create Payment endpoint.
3. Install your connector in a store and perform the homologation step. Here you will test each endpoint of your connector using the Payment Provider Test Suite app.
4. After your connector passes all the tests, open a ticket so our team can carry out the homologation process.</p>
