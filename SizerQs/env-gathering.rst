Discovery Questions
===================

When speaking with a customer there's a typical set of questions that can be used to open up the conversation when learning about the existing environment(s). Use these examples and walk through what an SE should be looking for over and above the answer(s).

What to look for in Server Virtualisation?
++++++++++++++++++++++++++++++++++++++++++

What would you look for?

-  Big RAM & vCPUs allocation - what's the impact to HA?

-  Guest OS version, this may be running older single threaded applications

-  CPU Commitment ratio / CPU Ready time, what is the impact?

-  Virtual machines using USB passthrough / USB over IP?

-  Virtual machine(s) license bound to MAC address

-  Opportunity for Xtract for VM

 
What to look for in VDI?
++++++++++++++++++++++++

What would you ask for when sizing VDI?

-  Density per node for desktops - thoughts?

-  Clock speed versus core quantity?

-  Where are the presentation services hosted?

-  File shares for user and departmental data

-  Applications being hosted in the desktop?


Calculating User Density per node
.................................
When calculating the user density per node a formula that is commonly used internally is:

``((Socket x Cores) x hyperthreading) +20% +15%) -CPU CVM) x CPU Overcommit``

The hyperthreading value is typically 1.3

Why +20%? – It’s the uplift in performance we’ve observed in our lab testing from IvyBridge chipset to Haswell when using LoginVSI

Why +15%? – It’s the uplift in performance we’ve observed in our lab testing from Haswell chipset to Broadwell when using LoginVSI

If the desktop virtual hardware profile requires 2 X vCPUs then reduce the user quantity by 20%, if it’s 3 – 4 vCPUs then 25%


Citrix XenApp server density calculation ‘guide’
................................................
When calculating a XenApp server density per node a formula that is commonly used internally.

``((((cores per node) x hyperthreading) x Haswell) x Broadwell) – CVM vCPUs) / vCPUs for the VM = VMs per node``

As above the percentage uplift for Haswell is +20%, Broadwell +15% Broadwell and hyperthreading ratio 1.3

Here’s an example assuming 36 cores total, 8 vCPUs for the CVM and 8 for the Windows guest OS VM:

``((((36) x 1.3) x 1.2) x 1.15)-8/8 = 7``


Database servers
++++++++++++++++
What would you look for?

-  Physical at the moment?

   -  DBAs may be nervous of virtualisation

   -  Share our Best Practice Guides / Reference Architectures

   -  Opportunity for Xtract for DBs

-  Big RAM & vCPUs allocation - what's the impact to HA?

-  Version of the database application

-  Rate of change per day
