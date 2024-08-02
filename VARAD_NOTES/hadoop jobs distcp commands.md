---
created: 2024-07-17T23:11
updated: 2024-08-02T16:35
---
**test**

```

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_attributes_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/address_attributes_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_cookies_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/address_cookies_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_headers_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/address_headers_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_ssl_certs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/address_ssl_certs_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_web_components_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/address_web_components_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_attributes_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/host_attributes_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_cookies_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/host_cookies_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_dependent_requests_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/host_dependent_requests_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_headers_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/host_headers_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_web_components_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/host_web_components_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_pairs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/host_pairs_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_ssl_certs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/host_ssl_certs_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/ssl_certs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseustestpub.dfs.core.windows.net/ssl_certs_aggregate/year=2024/month=202407/day=20240715/" &

------------------

nohup hadoop distcp -overwrite "wasbs://import@hostaxisstoragedeveast.blob.core.windows.net/ cve_summary/year=2024/month=202407/day=20240715/*" "abfss://internal@hostaxiseusprodint.dfs.core.windows.net/ cve_summary/year=2024/month=202407/day=20240715/" &

```

prod
--
```

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_attributes_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/address_attributes_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_cookies_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/address_cookies_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_headers_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/address_headers_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_ssl_certs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/address_ssl_certs_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/address_web_components_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/address_web_components_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_attributes_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/host_attributes_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_cookies_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/host_cookies_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_dependent_requests_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/host_dependent_requests_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_headers_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/host_headers_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_web_components_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/host_web_components_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_pairs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/host_pairs_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/host_ssl_certs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/host_ssl_certs_aggregate/year=2024/month=202407/day=20240715/" &

nohup hadoop distcp -overwrite "wasbs://published@hostaxisstoragedeveast.blob.core.windows.net/ssl_certs_aggregate/year=2024/month=202407/day=20240715/*" "abfss://published@hostaxiseusprodpub.dfs.core.windows.net/ssl_certs_aggregate/year=2024/month=202407/day=20240715/" &

------------------

nohup hadoop distcp -overwrite "wasbs://import@hostaxisstoragedeveast.blob.core.windows.net/ cve_summary/year=2024/month=202407/day=20240715/*" "abfss://internal@hostaxiseusprodint.dfs.core.windows.net/ cve_summary/year=2024/month=202407/day=20240715/" &

```