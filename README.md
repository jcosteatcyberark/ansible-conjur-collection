![](https://img.shields.io/badge/Certification%20Level-Community-EA0A8E?link=https://github.com/cyberark/community/tree/master/Conjur/conventions/certification-levels.md)
## CyberArk Ansible Conjur Collection

****

### cyberark.conjur-collection

This collection contains plugins to be used for CyberArk Conjur & DAP hosted in [ansible galaxy](https://galaxy.ansible.com/cyberark/conjur).

### Requirements

- [CyberArk Conjur Open Source](https://www.conjur.org) or
- [CyberArk Dynamic Access Provider](https://docs.cyberark.com/Product-Doc/OnlineHelp/AAM-DAP/Latest/en/Content/Resources/_TopNav/cc_Home.htm)

### Role Variables

None.
<br>
<br>

## Plugins

### conjur_variable Lookup Plugin

Fetch credentials from CyberArk Conjur using the controlling host's Conjur identity or environment variables.

- The controlling host running Ansible has a Conjur identity. [More Information here](https://docs.conjur.org/latest/en/Content/Get%20Started/key_concepts/machine_identity.html)
- Environment variables could be CONJUR_ACCOUNT, CONJUR_APPLIANCE_URL, CONJUR_CERT_FILE, CONJUR_AUTHN_LOGIN, CONJUR_AUTHN_API_KEY

#### Example Playbook

```yaml
---
  - hosts: localhost
  
    tasks:
  
      - name: Lookup variable in Conjur
        debug:
          msg: "{{ lookup('cyberark.conjur_collection.conjur_variable', '/path/to/secret') }}"
```

### Author Information
- CyberArk Business Development Technical Team 
    - @cyberark-bizdev
    - @enunez-cyberark
    - @jimmyjamcabd
