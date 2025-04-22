# 🛠️ VM Provisioning with Ansible + VMware + Infoblox

## 📌 Summary

Automated the provisioning of virtual machines using **Ansible**, **govc** (vSphere CLI), and **Infoblox** for IP address management. This project reduced manual provisioning time, ensured consistency across environments, and improved infrastructure deployment speed.

---

## 🔧 Tools & Technologies

- Ansible (custom playbooks)
- VMware vSphere + govc
- Infoblox (IPAM integration)
- Red Hat Enterprise Linux (RHEL)
- DNS / DHCP provisioning

---

## 🚀 Key Tasks Performed

- Created **Ansible playbooks** to:
  - Deploy new VM templates using `govc`
  - Customize guest OS settings (hostname, IP, DNS)
  - Register new entries to **Infoblox** via API
  - Perform post-deploy configuration (SSH, firewall rules, yum repo)

- Integrated with **Infoblox** API to automate:
  - IP allocation
  - DNS entry creation

- Implemented **Idempotency** for reruns
- Used **inventory grouping** to manage different environments (dev/stage/prod)

---

## 🤔 Challenges & Solutions

| Challenge | Solution |
|----------|----------|
| govc configuration was complex for new users | Created reusable Ansible roles to abstract the govc commands |
| Infoblox API rate limits | Batched IP requests and added retries with exponential backoff |
| Different template versions across clusters | Added dynamic inventory + validation step |

---

## 📈 Impact

- Provisioning time per VM: ⏱️ **reduced from ~30 minutes to <5 minutes**
- Consistency improved across all environments
- Reduced human error in DNS/DHCP assignment

---

## 🔍 Next Steps

- Add GitOps integration for provisioning via PR
- Integrate with CI/CD for environment spin-up
- Implement Terraform version of this setup

