# Ansible Role: Lynis

This role is a lynis-enterprise-role of toscom

## Requirements

- Ansible 2.1.0+ ( might work with prior versions too)
- Debian-based Linux-distribution

## Dependencies

None.

## Installation

```
git clone https://github.com/whotwagner/lynis-enterprise
```

## Role Variables

Some variables to change for enterprise installations:
```
lynis_licensekey: <YOUR-ENTERPRISE-LICENSE-KEY>
lynis_uploadserver: "portal.cisofy.com"
lynis_repo: "https://packages.cisofy.com/customers/{{lynis_licensekey}}/lynis/deb/"
```

If lynis_licensekey is false, the enterprise things won't be installed

### Configuration example


#### Standard Installation

```
- hosts: all
  become: yes
  roles: 
    - lynis-enterprise
```

# Licence

GPL

# Author information

TOSCOM [**(http://www.toscom.at/)**](http://www.toscom.at)
