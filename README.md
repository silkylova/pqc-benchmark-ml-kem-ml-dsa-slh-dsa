# PQC Benchmark: ML-KEM, ML-DSA, SLH-DSA

This repository contains the code and raw results for the paper:

> **Performance Benchmarking of NIST-Standardized Post-Quantum Cryptography Algorithms: A Comparative Study of ML-KEM, ML-DSA, and SLH-DSA**  
> Zhibek Mussakulova  
> Astana IT University, School of Cybersecurity

## What’s inside

- `pqc_benchmark.ipynb` – Google Colab notebook that:
  - builds and installs liboqs and liboqs-python,
  - runs benchmarks for ML-KEM, ML-DSA, SLH-DSA (all NIST security levels),
  - includes classical baselines RSA-2048 and ECDSA P-256,
  - saves mean and standard deviation for each operation.
- `pqc_results.json` – raw benchmark results (mean and standard deviation for all operations).

## How to run

1. Open the notebook in Google Colab (upload `pqc_benchmark.ipynb` to your Drive and open with Colab, or use “Open in Colab” if you set that up).
2. Run the first cell to install liboqs and liboqs-python (takes a few minutes).
3. Run the benchmark cell to re-generate `pqc_results.json` and the printed table.
4. Run the plotting cell to regenerate the figures.

All experiments were performed on Google Colab (x86-64, single-core, virtualized environment). Results should be interpreted as **relative performance indicators**, not absolute production-grade latencies.

## Relation to the paper

- The notebook implements exactly the methodology described in the paper:
  - 1,000 iterations per operation,
  - mean ± standard deviation,
  - ML-KEM (FIPS 203), ML-DSA (FIPS 204), SLH-DSA (FIPS 205, SHA2‑based “s” variants only),
  - classical baselines RSA-2048 and ECDSA P-256.
- The numbers in the paper are derived from runs of this notebook (or an equivalent version).

## Data and reproducibility

- `pqc_results.json` contains the full raw results (means and standard deviations) for all algorithms and operations.
- You can re-run the notebook to reproduce similar results on your own Colab session. Small differences are expected due to Colab’s shared, virtualized infrastructure.

## License

Code and data in this repository are provided under the [MIT License](LICENSE) 


## Contact
- Zhibek Mussakulova: mussakulovazhibek@gmail.com  
