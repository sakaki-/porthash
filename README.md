# porthash
Utility to compute, or verify (default), the signed hash of a Portage repo tree

## Description

**porthash** is a simple script that creates, or by default verifies, a signed `sha512` "master" hash of the specified Portage repostitory tree (by default, `/usr/portage`). It is intended to provide assurance - when distributing a repo snapshot over an unauthenticated channel such as rsync - that the consitutent ebuilds, manifests etc. have not been tampered with in transit.

The cascaded ("master") hash covers the contents of all files in the repository tree (excluding `distfiles/...`, `packages/...`, and `.git/...`) together with some metadata about these files and their containing directories (name, perms, type, owner, and group).

Please see the included manpage for further details.

## Installation

**porthash** is best installed (on Gentoo) via its ebuild, available as part of the [**sakaki-tools** overlay](https://github.com/sakaki-/sakaki-tools).
