## How to Fix Hive metastore db error

If you encounter this error:

`Unable to instantiate org.apache.hadoop.hive.ql.metadata.SessionHiveMetaStoreClient`

Please take the follow steps:

- Perhaps you forgot to run this hive setup script `/mnt/shared/uploads/setup_hive.sh`. Please run this script

- If the above script fails (e.g. `schemaTool failed`). Please try to remove  `~/hive/metastore_db` using

    ```bash
    rm -rf ~/hive/metastore_db  
    ```
- If the above step failed, please try to close all notebooks and terminals but the current one. The second icon (a circle with a square hole) on the left panel will show all the running notebooks and terminals with a "Shut down" button.

Please note that because Hive's metastore database is powered by a single-user embedded database called Derby, you cannot run two Hive instances at once. Be sure to close other instances of Hive (or Hive Shell) before you run Hive.


