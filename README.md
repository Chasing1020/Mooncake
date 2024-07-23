# Mooncake

## TransferEngine subsystem

### Quickstart

- Start memcached server (e.g. optane21:12345)

- Target node (optane21):

  ```
  ./example/net/example --mode=target --metadata_server=optane21:12345
  ```

- Initiator node (optane20):

  ```
  ./example/net/example --mode=initiator \
                             --threads=8 \
                             --metadata_server=optane21:12345 \
                             --operation=read|write \
                             --segment_id=optane20/cpu:0
  ```

You can get all flags in `example.cpp`.
