---
sidebar_label: Encryption
title: Encryption
sidebar_position: 2
---

## Overview

Encrypting a value with the component's key at different levels means the values need to be decrypted before they can be merged
It also means the decryption key comes from the several components that may lead to a context rather than just the context

it also needs to be at the component level if use can save values to the actual asset rather than those owned by the context
to make this work at the component rather than context just need to implement context_attrs

Also, if the components have their own values for e.g. domain, etc then they need to be able to encrypt
Rather than auto creating keys as needed the user should create a key manually. Each component yields to its parent if there is no key_file or key value

#### Encryption Keys
- all keys are in one file (config.data_home.join(keys.yml))
- the  component's attributes are used as the key in the file
- naming convention for encryption keys as ENVs
- CNFS_KEY  # Project
- CNFS_KEY_BACKEND
- CNFS_KEY_BACKEND_DEVELOPMENT

