---
sidebar_label: Intro
sidebar_position: 1
---

This guide covers getting up and running with Cloud Native Full Stack

:::info After reading this guide, you will know:

:heavy_check_mark: What is a Segment and how to configure the Root Segment and multiple child segments

:heavy_check_mark: What is an Asset and the three Asset types: Operator, Target and Generic

:heavy_check_mark: How cloudctl invokes tools to perform operations on targets

:heavy_check_mark: How to quickly generate assets for your project
:::

## Overview

- Segments are used to organize your project. Segments contain assets and optionally additional segments. Each project comes with a default root segment
- Assets belong to segments and are one of three types: Operator, Target and Generic
- Operators 'operate' or perform actions on Targets. For example, Docker Compose is an Operator that starts and stops (the actions) services (the Target)
