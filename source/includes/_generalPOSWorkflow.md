##POS workflow - general overview
There is a complex workflow in the background which involves many moving parts, as it can be seen on diagram below. The general POS workflow will be presented here, however in the section below, specific use cases are provided which should help you with integration process with Product36 platform, regardless of your business requirements.

Although the diagram shows variant in which user pays to the merchant using phone QR code reader or by entering the address manually (very unlikely), this model can be used in any other process. Address which is retrieved from the system can be presented to user in any preferable way. 

There are two types of addresses that can be given by the system. One is normal address which does not have expiration time. Another one is so called autosell address which is tightly bound to FIAT currency. This option cannot be defined within call, as it has to be configured in the main application. Autosell address is time bound.

Number of notifications required to assume that the transaction is successfully committed is defined by the policies in the main application and cannot be changed by the third parties.

![POS workflow](/images/image2.png)

Every POS from the system standpoint has to implement states shown on the following diagram. POS is handled through main system interface and can be enabled, disabled or deleted either by merchant or system administrator. In order to be used, POS needs appropriate non-opaque API key.
