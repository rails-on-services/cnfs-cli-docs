---
sidebar_label: Interpolation
title: Interpolation
sidebar_position: 3
---

## Overview

- parent and self inside ${}
- Component has method as_merged which is the merged values of all components in its hierarchy that are cnfs_subbed
- Another method for component is to_context which is as_merged

cnfs_sub takes an array of objects for which it will search for the interpolation. If it's not found in any of the references then it logs a warning
All YAML should be able to be encrypted and cnfs_subed

assets are cnfs_sub'ed against their inheriteds and their owner (component)
components are cnfs_subed against
