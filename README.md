# thoughts-on-trino-iceberg-storage

Trino, iceberg storage

* Virtual columns (view level), can't participate in uniqueness 
* Option on whether to allow filters on virtual columns. Explicit notion on performance degradation
* Functional columns (physically stored, updated only on create, update or explicit request), can participate in uniqueness
* On partial updates, if some fields touch uniqueness indexes all other fields required to compute such index should be provided. It includes functional columns, if it participates in uniqueness all fields required to compute it should be provided
