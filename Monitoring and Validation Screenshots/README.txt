Monitoring and Validation Screenshots
These figures demonstrate the real-time monitoring, request load distribution, CPU usage, memory tracking, and service deployment status captured during the deployment and evaluation of the hybrid autoscaling system.

1. Prometheus – CPU Usage per Pod

This stacked area graph shows the sum of container CPU usage per pod over a 1-hour window, updated every minute. It captures dynamic fluctuations and occasional spikes, providing critical input for Phase 2 CPU forecasting.

2. Prometheus – Request Rate per Pod (Istio Metrics)

The graph illustrates aggregated request rate (istio_requests_total) per pod. The data reflects traffic variability across services and serves as the primary input for Phase 1 request forecasting.

3. Kubernetes Dashboard – Pod Overview

This screenshot presents the Kubernetes dashboard showing real-time CPU and memory usage of selected microservices (e.g., currencyservice, recommendationservice, frontend). It verifies the system's responsiveness and pod health under varying loads.

4. Prometheus – Early Request Surge Visualization

A sharp increase in request rate is observed around 09:55 AM, which demonstrates the system’s ability to detect and respond to traffic bursts. This data supports testing of the forecasting system’s latency handling.

5. Prometheus – CPU Spike Analysis

A brief CPU usage spike is recorded at 10:10 AM. This illustrates real-time load stress on pods, a critical case for evaluating the autoscaler’s responsiveness.

6. Prometheus – Memory Usage per Pod

This graph shows total memory consumption per pod in bytes. The step increase reflects container provisioning events, and highlights opportunities for extending the forecast model to support memory-based scaling.

7. Prometheus – Request Throughput Over Time

The chart captures sustained request throughput per pod, indicating load stability and the system's ability to manage continuous user interactions.

8. Prometheus – Autoscaling Event Triggered by Load Spike

Another CPU usage spike is shown, followed by a downward correction—an example of the autoscaling logic mitigating resource saturation.

9. Prometheus – Memory Scaling Activity

The memory usage graph shows step-wise increases, indicating memory-bound pod provisioning events. This highlights the importance of extending autoscaling to multi-resource dimensions.

10. Kubernetes Dashboard – Deployments Overview

A top-level view of all deployments and associated pods within the default namespace. It confirms successful microservice rollout (12 deployments, 24 pods), ensuring a consistent testbed for autoscaling validation.
