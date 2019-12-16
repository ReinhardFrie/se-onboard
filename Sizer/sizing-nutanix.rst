Sizing with Sizer (and without)
===============================

Sizing Nutanix successfully is driven purely from the data gathered from a customer and the SE's understanding of the customer's intended solution. The Nutanix Sizer tool provides an easy to follow wizard driven input method but sometimes quick number crunching while on-site can be useful.


Data gathering
++++++++++++++
*Objective: promote the key areas where data extraction influences the design*

Explore the customer's environment with these sample questions

-  Data gathering

   -  Application(s) hosted the on virtualised estate

   -  Current hardware deployment(s)

   -  Quantity of DCs

   -  LAN / WAN (including bandwidth and latency)

   -  Current hypervisor(s) and management tool(s)

   -  vCPU / RAM / Disk

   -  BCP and DR

      -  Today

      -  Aspiration

   -  Backup

      -  Rate of change (daily)

- Tools

  - VMware environments can be scanned using a free tool called RVTools, this outputs all details of the VMs to a .CSV file which can be imported directly into Nutanix Sizer

  - Dell's DPACK can scan and capture physical and virtual workloads over a period time providing utilisation metrics, better for environments where peak workload processing periods need to be taken into consideration



Nutanix Sizer walkthrough
+++++++++++++++++++++++++
*Objective: demonstrate Nutanix Sizer*

-  Create a first pass BoM for general server virtualisation and discuss these influential areas

   -  HA (N+1, etc...)

   -  vCPU : pHTcore ratio

   -  RAM density choice

   -  SSD balance


-  Review the graphs and discuss the outputs and reports


Manual Sizing walkthrough
+++++++++++++++++++++++++
*Objective: follow a manual sizing exercise to prepare an SE for on-the-fly whiteboard BoM creation*

Run through a scenario using paper or a whiteboard

-  Show how a customer's CPU, RAM and storage requirements can quickly steer the design in a first pass



Replaying back the solution to the customer
+++++++++++++++++++++++++++++++++++++++++++
*Objective: items that should ideally be presented back to the customer as part of the solution*

-  SpecInt baseline of the existing customer kit versus the proposed solution

-  Document your assumptions and constraints
