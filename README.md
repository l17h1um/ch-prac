# ch-prac

## Квик старт

https://clickhouse.com/docs/ru/getting-started/quick-start

```
curl https://clickhouse.com/ | sh
ls
./clickhouse start
./clickhouse client
```

```
CREATE TABLE my_first_table
(
    user_id UInt32,
    message String,
    timestamp DateTime,
    metric Float32
)
ENGINE = MergeTree
PRIMARY KEY (user_id, timestamp)
```

```
INSERT INTO my_first_table (user_id, message, timestamp, metric) VALUES
    (101, 'Hello, ClickHouse!',                                 now(),       -1.0    ),
    (102, 'Insert a lot of rows per batch',                     yesterday(), 1.41421 ),
    (102, 'Sort your data based on your commonly-used queries', today(),     2.718   ),
    (101, 'Granules are the smallest chunks of data read',      now() + 5,   3.14159 )
```

```
wget 'https://drive.google.com/uc?id=1N1xoxgcw2K3d-49tlchXAWw4wuxLj7EV&export=download' -O output.csv
```
