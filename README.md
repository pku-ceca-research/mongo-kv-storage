#Mongo KV Storage Project

## Project Managment

We intend to organize the whole project directory like this:

1. `mongo`: A git submodule that has a remote repository on [github](https://github.com/pku-ceca-research/mongo.git`), which is forked from the lasted mongodb repo.
2. `mongo/src/third_party/rocksdb`: Latest RocksDB source code [directory](https://github.com/facebook/rocksdb). We need to link this to build the storage engine.
3. `mongo/src/mongo/db/modules/rocks`: The `mongo-rocks` [integration](https://github.com/pku-ceca-research/mongo-rocks.git). This one will also be fetched from our repository, as the original one has several conflicts with the current mongodb version.
4. `mongo/src/mongo/db/modules/kvs`: This should be our integration code with the KVS standard API. We should define this later.

The listing 2,3,4 will not be "right in" the `mongo/` directory, in order to keep clean and simple. They will lies in this repository and when you run the install procedure, they will be automatically integrated.
