# Outline for the project [Testing the support and interoperability of Zarr Zip Stores](https://www.outreachy.org/outreachy-december-2022-internship-round/) by [Weddy Gikunda](https://github.com/caviere) for Outreachy December 2022 Cohort

# About me
* Name: Weddy Gikunda
* Website: https://caviere.github.io/
* Location: Nairobi,Kenya

# Project Information

Zarr is an open-source data format for storing chunked, compressed N-dimensional arrays. Zarr is based on an open technical specification, making implementations across several languages possible. One of the methods inside zarr.storage is ZipStore, which essentially stores Zarr arrays and groups using a Zip file. For this project, we would like to test the support and interoperability of ZipStores among various Zarr implementations. We’d also like to check and see the existing functionality of zarr-python’s ZipStores and compare it with ZipStores in other Zarr implementations. 

# Related links: 
1. [Zarr/storage.py](https://github.com/zarr-developers/zarr-python/blob/main/zarr/storage.py)
2. [Zarr ZipStore](https://zarr.readthedocs.io/en/stable/api/storage.html#zarr.storage.ZipStore)

# Contribution Phase Work
* Proposed using the “visit” method to implement “find” and “findall” rather than having separate methods for the same. This ensures the API does not get bloated. Here is the link to the github [discussion](https://github.com/zarr-developers/zarr-python/issues/188) I participated in and the [merged PR](https://github.com/zarr-developers/zarr-python/pull/1241)
* Found and fixed various errors and bugs in the Zarr codebase - Here is the [PR](https://github.com/zarr-developers/zarr-python/pull/1226)

# Tasks Done
* Going through the existing zarr codebase.
* [Created a ZipStore in zarr-python and tested the support across various Zarr implementations](https://github.com/caviere/testing_zipstore)
* [Created a MNIST Dataset script](https://github.com/caviere/testing_zipstore/blob/main/py/example.py)
* [Created a benchmark script that reads and writes Zarr arrays using directory, zip and fsspec stores](https://github.com/caviere/testing_zipstore/blob/main/benchmark/main.py)
* [Created a script that benchmarks the timings it takes to fetch data from a zipstore, LRU cache and in memory store using uniform and zipfian distributions](https://github.com/caviere/testing_zipstore/tree/main/cache)
