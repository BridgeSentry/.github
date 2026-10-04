# BridgeSentry

This organization hosts the code and results for the paper **"BridgeSentry: Meta-Path-Guided
Graph Learning for Cross-chain Bridge Attack Detection."**

## Repositories

- **[XChainDataGen](https://github.com/BridgeSentry/XChainDataGen)** - Fork of
  [XChainDataGen](https://github.com/AndreAugusto11/XChainDataGen) extended to extract
  cross-chain bridge activity (including additional bridges/chains) and convert it into
  heterogeneous graph data, stored in a PostgreSQL database.

- **[BridgeSentry](https://github.com/BridgeSentry/BridgeSentry)** - The detector itself: reads the
  graph data produced by XChainDataGen and trains/evaluates a heterogeneous GNN to classify
  transactions as normal or anomalous. Two variants live on separate branches
  (`bridgesentry-c`: supervised classifier; `bridgesentry-sad`: Deep SAD-based anomaly detection).

- **[BridgeSentry-Results](https://github.com/BridgeSentry/BridgeSentry-Results)** - Experiment
  outputs (metrics, logs, trained artifacts) produced by running BridgeSentry, kept separate
  from the code repo to avoid bloating it.

## Execution Pipeline

1. XChainDataGen (to PostgreSQL)
2. BridgeSentry
