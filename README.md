# grpc-data-transfer

Trying out azure apim self hosted gateway.
This POC would use arrow flight as a grpc protocol and expose that api via azure apim with self hosted gateway.

The data used is in parquet format from here: 
* https://www.tablab.app/view/parquet?datatable-source=demo-flights-1m


This is done to have large dataset size so that it becomes a good simulation for real-world scenarios on transfering relatively large datasets.


Tech Stack:
- python : 3.11.5
- docker : 20.10.12
- kubernetes : 1.29.2 (AKS)
- APIM : Self Hosted Gateway (gateway hosted in AKS)


### Getting Started

The repository contains all the data needed to setup AKS, ACR, APIM and self-hosted-gateway in Azure.
Also it contains the relevant code to create container-image and to deploy the same onto AKS.
The container-image is pushed onto ACR registry.


### Directory Structure

```
client
    |
    |-- client.py (client to read data from grpc api)
grpc_api
    |
    |-- grpc api to be pushed onto ACR and deploy to AKS.
self-hosted-gateway
    |
    |-- code related to build self-hosted-gateway image and deploy that to AKS.
infra
    |
    |-- AKS (infra code for AKS)
    |-- APIM (infra code for APIM)


```