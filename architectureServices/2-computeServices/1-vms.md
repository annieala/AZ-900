With azure VM you can run virtualized serves in azure as infrastructure as a service. like a physical server you control the operating system and installed software.

VM are a good fit when you need:

Total control over the operating system (OS).
The ability to run custom software.
To use custom hosting configurations.

Azure VMs remove the need to buy and maintain physical server hardware. As an IaaS service, you still manage patching, updates, and configuration inside the VM.

You can deploy VMs quickly from prebuilt images. An image is a template that already includes an operating system and tools such as web hosting components.

examples of when to use vms

testing and development: create different os and app configurations quickly then remove the vm when testing is complete

cloud application hosting run applications in azure and scale capacity up or down as demand changes

data center extension; extend an on premises network into azure and host workloads in a connected virtual network,

disaster recovery, keep failover capacity in azure and run ciritical workloads there if your primary site is unavailable

lift and shift mightations- move existing server workloads with minimal application redesign

VM resources and sizing

- when you provision a vm you choose resources such as
- size (purpose, number of processor cores and amount of ram
  -networking (virtual network public ip address and port configuration

understand vm size families and names
azure vm sizes are grouped into families so you can quickly choose a size based on your workload needs

vm size families
choose the family that best matches workload behavior

b - burstable
d - general
e - memor
f - comput
m - large memor
l - storage
n - gpu

vm options vCPU, RAM Disk Netowrk, Premium SSD, Generation

vCPU count affects comput capacity for concurrent and CPU Bound workloads
RAM: affects how much working data the VM can keep in memory.
Disk configuration: affects storage capacity, IOPS, and throughput.
Network throughput: affects data transfer performance in and out of the VM.
Premium SSD support: indicates whether the size supports premium managed disks.
Hardware generation: indicates platform generation and can affect baseline performance.

D - VM family
2: number of cpus in this size
s: supports premium ssd storage
v5: hardware generation for that family

At a fundamentals level, start by selecting a family that matches workload behavior, then choose the size that meets performance needs and scale as demand grows.

Scale and resiliency options for VMs
You can run single VMs for testing, development, or minor tasks. Or you can group VMs together to provide high availability, scalability, and redundancy. Azure can manage these groupings with features such as scale sets and availability sets.

Virtual machine scale sets
Virtual machine scale sets let you create and manage groups of identical, load-balanced VMs. Without scale sets, you must manually keep VM configuration consistent, monitor utilization, and adjust instance counts. Scale sets centralize configuration and can automatically scale out or in based on demand or schedules. They also integrate with load balancing so traffic is distributed efficiently.

Virtual machine availability sets
Virtual machine availability sets improve VM resiliency inside a region. They reduce the chance that all VMs are affected by one maintenance event or hardware failure.

Availability sets group VMs by:

Update domain: VMs that can be rebooted together during planned maintenance.
Fault domain: VMs that share a potential power or network failure point.
Use availability sets for VM-level redundancy. In regions that support Availability Zones, zone-based designs are often preferred because they provide broader failure isolation. Availability sets themselves don't add cost; you pay for the VM instances.

Scale and resiliency options for VMs
You can run single VMs for testing, development, or minor tasks. Or you can group VMs together to provide high availability, scalability, and redundancy. Azure can manage these groupings with features such as scale sets and availability sets.

Virtual machine scale sets
Virtual machine scale sets let you create and manage groups of identical, load-balanced VMs. Without scale sets, you must manually keep VM configuration consistent, monitor utilization, and adjust instance counts. Scale sets centralize configuration and can automatically scale out or in based on demand or schedules. They also integrate with load balancing so traffic is distributed efficiently.

Virtual machine availability sets
Virtual machine availability sets improve VM resiliency inside a region. They reduce the chance that all VMs are affected by one maintenance event or hardware failure.

Availability sets group VMs by:

Update domain: VMs that can be rebooted together during planned maintenance.
Fault domain: VMs that share a potential power or network failure point.
Use availability sets for VM-level redundancy. In regions that support Availability Zones, zone-based designs are often preferred because they provide broader failure isolation. Availability sets themselves don't add cost; you pay for the VM instances.
