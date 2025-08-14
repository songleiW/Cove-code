# **Cove: A System for Oblivious Community Search on Outsourced Streaming Graphs**

## **Overview**

Cove is a system designed for oblivious community search over outsourced streaming graphs. It enables secure community search on graph data stored in the cloud, while maintaining privacy and confidentiality. By utilizing cryptographic techniques such as secret sharing, Cove ensures that no sensitive information about the graph or query is leaked during the search process.

This repository contains the source code for the Cove system, which provides efficient and privacy-preserving methods for community detection, particularly in real-time streaming graphs. The system employs a distributed trust model where three independent cloud servers work together to protect user data.

## **Features**

* **Oblivious Community Search**: Perform community search over a streaming graph without revealing the graph structure, the query vertex, or the detected communities to the cloud servers.
* **Privacy-Preserving**: Uses cryptographic techniques such as secret sharing and oblivious message passing to ensure the privacy of the data.
* **Efficient**: Achieves significant speedup and reduced server-side communication compared to existing methods built on generic secure multiparty computation frameworks.
* **Real-Time Graph Processing**: Designed to handle continuously evolving graph data, making it suitable for applications such as fraud detection, social network analysis, and contact tracing.

## **Installation**

### Prerequisites

* Python 3.6 or higher
* Required Python libraries (listed below)

### Steps

1. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Ensure that you have the necessary cryptographic libraries and tools installed to support secret sharing and encryption.

## **Usage**

1. **Data Input**: The system takes in graph data in the form of a streaming graph. You can provide your own dataset, or use the pre-generated sample datasets included in the `data` folder.

2. **Run the System**: To perform community search on your dataset, run the following command:

   ```bash
   python run_cove.py --input_graph path/to/your/graph --query_vertex your_query_vertex
   ```

3. **Parameters**:

   * `input_graph`: The path to your graph dataset (in edge list format).
   * `query_vertex`: The vertex around which the community search will be performed.
   * Additional parameters for graph processing (e.g., radius, thresholds) can be passed as arguments.

## **Example**

```bash
python run_cove.py --input_graph data/sample_graph.edgelist --query_vertex 5 --radius 2 --k_c 3 --k_f 2
```

This command will perform a community search around vertex 5 with a radius of 2, looking for communities that meet the truss community thresholds of `k_c=3` and `k_f=2`.

## **Contributing**

We welcome contributions to improve and extend the system. If you have suggestions or would like to contribute code, please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
