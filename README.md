# PyQualtrics

This repo contains a `Dockerfile` to build
a Linux [Docker](https://www.docker.com) image containing the Microsoft
[SQL Server Tools](https://docs.microsoft.com/en-us/sql/linux/sql-server-linux-setup-tools?view=sql-server-linux-2017)
and package for Linux. The image also includes Microsoft's
[ODBC driver for SQL Server](https://docs.microsoft.com/en-us/sql/connect/odbc/microsoft-odbc-driver-for-sql-server?view=sql-server-linux-2017)
and a working Python 3.7 environment based on the
[Miniconda](https://conda.io/miniconda.html)
environment management system developed by
[Anaconda, Inc](https://www.anaconda.com/). The Python environment includes the
[py_qualtrics_api](https://github.com/blueogive/py_qualtrics_api) package, which
is a fork of [py_qualtrics_api](https://github.com/cwade/py_qualtrics_api) for
interacting with the
[Qualtrics](https://www.qualtrics.com) [API](https://api.qualtrics.com/). The
image is designed to facilitate devops pipelines that include operations on
the Qualtrics platform.


## Usage

To instantiate an ephemeral container from the image, mount the current
directory within the container, and open a bash prompt within the `base` conda
Python environment:

```bash
docker run -it --rm -v $(pwd):/home/docker/work blueogive/py_qualtrics_api:latest
```

Contributions are welcome.
