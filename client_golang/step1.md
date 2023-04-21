This is interactive playground.

Please follow task in [slides](https://docs.google.com/presentation/d/1-LauyQqDQD5a1oAk16Ke03uKGwgH5UT0hBuy7aIwJIg/edit).

Particularly:

1. Clone client_golang

    ```
    git clone git@github.com:prometheus/client_golang.git
    ```{{exec}}
   
2. Go to whatup dir:

    ```
    cd tutorial/whatsup
    ```{{exec}}
   
3. Run Prometheus and Jaeger in Background:

    ```
    make init
    ```{{exec}}

(make stop to stop it)

4. Modify and run main.go

    ```
    make run
    ```{{exec}}

(Ctrl+C to stop it)

Now you can in separate terminal:

* Get main.go metrics to explore

    ```
    make metrics
    ```{{exec}}

* Open Prometheus UI and query metrics [ACCESS PORTS]({{TRAFFIC_SELECTOR}})
* Run acceptance tests to verify your progress.

    ```
    make test
    ```{{exec}}


## Task

Modify main.go to have:

- Scrape Endpoint
- whatsup_queries_handled_total (counter)
- whatsup_last_response_elements (gauge)
- build_info (info gauge)
- whatsup_queries_duration_seconds (histogram)
- go_goroutines (gauge)
