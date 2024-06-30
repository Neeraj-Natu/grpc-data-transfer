# azure-data-transfer

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