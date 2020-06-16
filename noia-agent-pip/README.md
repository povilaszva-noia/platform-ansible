# Ansible Role: Docker

## Requirements

None.

## Role Variables

Available variables are listed (see `vars/main.yml`):

    # Required parameters
    NOIA_API_KEY: "YOUR_API_KEY"
    # Optional parameters
    NOIA_CONTROLLER_URL: "app-controller-platform-agents.noia.network"
    NOIA_ALLOWED_IPS: "[]"
    #If using docker , NOIA_NETWORK_API=docker would allow agent to access docker networks for information.
    NOIA_NETWORK_API: "none"
    NOIA_NAME: "Agent name"
    NOIA_COUNTRY: "Germany"
    NOIA_CITY: "Frankfurt"
    #Select one of the categories from the list or default will be assigned
    # 'IoT','Server','none'
    NOIA_CATEGORY: "IoT"
    #Select one of providers from the list or default will be assigned
    #'AWS', 'DigitalOcean', 'Microsoft Azure', 'Rackspace', 'Alibaba Cloud',
    #'Google Cloud Platform', 'Oracle Cloud', 'VMware', 'IBM Cloud', 'Vultr'.
    NOIA_PROVIDER: "Microsoft Azure"
    NOIA_LAT: "40.14"
    NOIA_LON: "-74.21"
    NOIA_TAGS: "Tag1,Tag2"


## Use with Ansible (and `docker` Python library)

```yaml
- hosts: all

  vars:
    NOIA_API_KEY: "YOUR_API_KEY"
    NOIA_CONTROLLER_URL: "app-controller-platform-agents.noia.network"
    NOIA_ALLOWED_IPS: "[]"
    NOIA_NETWORK_API: "none"
    NOIA_NAME: "Agent name"
    NOIA_COUNTRY: "Germany"
    NOIA_CITY: "Frankfurt"
    NOIA_CATEGORY: "IoT"
    #Select one of providers from the list or default will be assigned
    #'AWS', 'DigitalOcean', 'Microsoft Azure', 'Rackspace', 'Alibaba Cloud',
    #'Google Cloud Platform', 'Oracle Cloud', 'VMware', 'IBM Cloud', 'Vultr'.
    NOIA_PROVIDER: "Microsoft Azure"
    NOIA_LAT: "40.14"
    NOIA_LON: "-74.21"
    NOIA_TAGS: "Tag1,Tag2"

  roles:
    - noia.agent-pip
```

## Dependencies

None.
