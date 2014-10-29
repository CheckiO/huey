huey integration to CheckiO

backends/redis_backend.py changes:

    RedisBlockingQueue object:
        - changed "read" method (brpop to brpoplpush);
        - changed "remove" method;


api.py changes:
    Huey object:
        - added "remove_from_processing_list" method


consumer.py changes:
    WorkerThread object:
        - changed "process_task" method


constants.py changes (file was added):
    added "PROCESSING_LIST_QUERY" variable
