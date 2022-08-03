1. Modify pg_hba.conf declarations
2. add worker nodes to coordinator manually using
   ```
   psql 'host=citus-coordinator user=postgres' -c "SELECT * from citus_add_node('${HOSTNAME}.citus-worker.default.svc.cluster.local', 6432);"
   ```
