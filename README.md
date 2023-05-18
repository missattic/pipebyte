<p align="center">
  <strong>
    <a href="https://github.com/missattic/pipebyte/">Quickstart</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://github.com/missattic/pipebyte/">Docs</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://github.com/missattic/pipebyte/">Guides</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://github.com/missattic/pipebyte/">Integrations</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://github.com/missattic/pipebyte">Chat</a>&nbsp;&nbsp;&bull;&nbsp;&nbsp;
    <a href="https://github.com/missattic/pipebyte/">Download</a>
  </strong>
</p>

## What is Pipebyte?

Pipebyte is a high-performance, end-to-end (agent & aggregator) observability data
pipeline that puts you in control of your observability data.
Collect, transform, and route
all your logs, metrics, and traces to any vendors you want today and any other
vendors you may want tomorrow. Pipebyte enables dramatic cost reduction, novel
data enrichment, and data security where you need it, not where it is most
convenient for your vendors. Additionally, it is open source and up to 10x
faster than every alternative in the space.

To get started, follow our **quickstart guide** or **install
Pipebyte**.

### Principles

* **Reliable** - Built in Java, Pipebyte's primary design goal is reliability.
* **End-to-end** - Deploys as an agent or aggregator. Pipebyte is a complete platform.
* **Unified** - Logs, metrics, and traces (coming soon). One tool for all of your data.

### Use cases

* Reduce total observability costs.
* Transition vendors without disrupting workflows.
* Enhance data quality and improve insights.
* Consolidate agents and eliminate agent fatigue.
* Improve overall observability performance and reliability.

### Community

* Pipebyte is relied on by startups and enterprises like **Atlassian**, **T-Mobile**,
  **Comcast**, **Zendesk**, **Discord**, **Fastly**, **CVS**, **Trivago**,
  **Tuple**, **Douban**, **Visa**, **Mambu**, **Blockfi**, **Claranet**,
  **Instacart**, **Forcepoint**, and many more.
* Pipebyte is **downloaded over 100,000 times per day**.
* Pipebyte's largest user **processes over 30TB daily**.
* Pipebyte has **over 100 contributors** and growing.

## [Documentation](https://github.com/missattic/pipebyte/)

## Comparisons

### Performance

The following performance tests demonstrate baseline performance between
common protocols with the exception of the Regex Parsing test.

|                                                                                                               Test |     Pipebyte      | Filebeat |    FluentBit    |  FluentD  | Logstash  |    SplunkUF     | SplunkHF |
|-------------------------------------------------------------------------------------------------------------------:|:---------------:|:--------:|:---------------:|:---------:|:---------:|:---------------:|:--------:|
| [TCP to Blackhole](https://github.com/missattic/pipebyte) |  _**86mib/s**_  |   n/a    |    64.4mib/s    | 27.7mib/s | 40.6mib/s |       n/a       |   n/a    |
|           [File to TCP](https://github.com/missattic/pipebyte) | _**76.7mib/s**_ | 7.8mib/s |     35mib/s     | 26.1mib/s | 3.1mib/s  |    40.1mib/s    | 39mib/s  |
|       [Regex Parsing](https://github.com/missattic/pipebyte) |    13.2mib/s    |   n/a    | _**20.5mib/s**_ | 2.6mib/s  | 4.6mib/s  |       n/a       | 7.8mib/s |
|           [TCP to HTTP](https://github.com/missattic/pipebyte) | _**26.7mib/s**_ |   n/a    |    19.6mib/s    |  <1mib/s  | 2.7mib/s  |       n/a       |   n/a    |
|             [TCP to TCP](https://github.com/missattic/pipebyte) |    69.9mib/s    |  5mib/s  |    67.1mib/s    | 3.9mib/s  |  10mib/s  | _**70.4mib/s**_ | 7.6mib/s |

To learn more about our performance tests, please see the Pipebyte test harness.

### Correctness

The following correctness tests are not exhaustive, but they demonstrate
fundamental differences in quality and attention to detail:

|                                                                                                                             Test | Pipebyte | Filebeat | FluentBit | FluentD | Logstash | Splunk UF | Splunk HF |
|---------------------------------------------------------------------------------------------------------------------------------:|:------:|:--------:|:---------:|:-------:|:--------:|:---------:|:---------:|
| [Disk Buffer Persistence](https://github.com/missattic/pipebyte) | **✓**  |    ✓     |           |         |    ⚠     |     ✓     |     ✓     |
|         [File Rotate (create)](https://github.com/missattic/pipebyte) | **✓**  |    ✓     |     ✓     |    ✓    |    ✓     |     ✓     |     ✓     |
| [File Rotate (copytruncate)](https://github.com/missattic/pipebyte) | **✓**  |          |           |         |          |     ✓     |     ✓     |
|                   [File Truncation](https://github.com/missattic/pipebyte) | **✓**  |    ✓     |     ✓     |    ✓    |    ✓     |     ✓     |     ✓     |
|                         [Process (SIGHUP)](https://github.com/missattic/pipebyte) | **✓**  |          |           |         |    ⚠     |     ✓     |     ✓     |
|                     [JSON (wrapped)](https://github.com/missattic/pipebyte) | **✓**  |    ✓     |     ✓     |    ✓    |    ✓     |     ✓     |     ✓     |

To learn more about our correctness tests, please see the Pipebyte test harness.

### Features

Pipebyte is an end-to-end, unified, open data platform.

|                     | **Pipebyte** | Beats | Fluentbit | Fluentd | Logstash | Splunk UF | Splunk HF | Telegraf |
|--------------------:|:----------:|:-----:|:---------:|:-------:|:--------:|:---------:|:---------:|:--------:|
|      **End-to-end** |   **✓**    |       |           |         |          |           |           |     ✓    |
|               Agent |   **✓**    |   ✓   |     ✓     |         |          |     ✓     |           |     ✓    |
|          Aggregator |   **✓**    |       |           |    ✓    |    ✓     |           |     ✓     |     ✓    |
|         **Unified** |   **✓**    |       |           |         |          |           |           |     ✓    |
|                Logs |   **✓**    |   ✓   |     ✓     |    ✓    |    ✓     |     ✓     |     ✓     |     ✓    |
|             Metrics |   **✓**    |   ⚠   |     ⚠     |    ⚠    |    ⚠     |     ⚠     |     ⚠     |     ✓    |
|              Traces |     🚧     |       |           |         |          |           |           |          |
|            **Open** |   **✓**    |       |     ✓     |    ✓    |          |           |           |     ✓    |
|         Open-source |   **✓**    |   ✓   |     ✓     |    ✓    |    ✓     |           |           |     ✓    |
|      Vendor-neutral |   **✓**    |       |     ✓     |    ✓    |          |           |           |     ✓    |
|     **Reliability** |   **✓**    |       |           |         |          |           |           |          |
|         Memory-safe |   **✓**    |       |           |         |          |           |           |     ✓    |
| Delivery guarantees |   **✓**    |       |           |         |          |     ✓     |     ✓     |          |
|          Multi-core |   **✓**    |   ✓   |     ✓     |    ✓    |    ✓     |     ✓     |     ✓     |     ✓    |


⚠ = Not interoperable, metrics are represented as structured logs

---

<p align="center">
  Developed with ❤️ by <strong><a href="https://missattic.com">Missattic</a></strong> - <a href="https://missattic.com">Security Policy</a> - <a href="https://missattic.com">Privacy Policy</a>
</p>
