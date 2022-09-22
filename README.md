# Google Summer of Code 2022

**Project page**: [Porting CRIU Image Tool (CRIT) to Go](https://summerofcode.withgoogle.com/archive/2022/projects/YberDUGn)
<br>
**Organisation**: [CRIU](https://criu.org)
<br>
**Mentor**: [Radostin Stoyanov](https://github.com/rst0git)
<br>
**Proposal**: [Prajwal S N - CRIU (GSoC 2022)](https://github.com/snprajwal/gsoc-2022/blob/main/Prajwal%20S%20N%20-%20CRIU%20%28GSoC%202022%29.pdf)

# Overview

CRIU provides a Python-based tool called CRIT in order to explore and manipulate checkpoint images. To enable hassle-free integration with Go projects, it is necessary to provide Go bindings for performing read/write/encode/decode operations on the image ﬁles. This project aims to extend the go-criu library to perform all image-based operations that CRIT is currently used for, both as an import-and-use dependency as well as a standalone CLI application. This will allow Go projects that use CRIU to perform better analysis and testing on checkpoint images without setting up any additional infrastructure.

# Implementation

- The list of features along with a brief explanation of the language-specific implementation is present in this [PR](https://github.com/checkpoint-restore/go-criu/pull/66)
- The complete details of the implementation can be found in the proposal [linked above](#google-summer-of-code-2022)
- The technical challenges faced while building this library are explained in [this blog post](https://snprajwal.com/tech/gsoc-journey)
- The documentation for the library is available [here](https://criu.org/CRIT_(Go_library))

# Pull requests

- [`go-criu#66` Port CRIT functionalities](https://github.com/checkpoint-restore/go-criu/pull/66)
- [`go-criu#76` Add docs and tests for CRIT](https://github.com/checkpoint-restore/go-criu/pull/76)

# Impact

This library is used in various open-source projects:

- [`runc#3586` Upgrade go-criu to v6](https://github.com/opencontainers/runc/pull/3586)
- [`podman#15591` Upgrade go-criu to v6](https://github.com/containers/podman/pull/15591)
- [`checkpointctl#16` Upgrade go-criu to v6](https://github.com/checkpoint-restore/checkpointctl/pull/16)
- [`lxd#10969` lxd: use go-criu/crit for dump statistics](https://github.com/lxc/lxd/pull/10969)

# Acknowledgements

I would like to thank my mentor Radostin for his encouragement, constant support, and perspectives. The resources he provided introduced me to novel concepts that I did not know existed and gave me the opportunity to read some phenomenal research papers. My knowledge of systems programming and the Linux ecosystem skyrocketed along the course of this project. I extend my gratitude to the GSoC team at Google for making it possible to contribute and work with this amazing team of people from across the world.

I would also like to thank the [mdpdf](https://github.com/bluehatbrit/mdpdf) project for enabling me to conveniently generate PDFs from markdown.
