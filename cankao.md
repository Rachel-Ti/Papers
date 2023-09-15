- [CCFA](#ccfa)
  - [Conference](#conference)
    - [ASPLOS](#asplos)
      - [2022](#2022)
        - [1.IceBreaker: Warming Serverless Functions Better with Heterogeneity](#1icebreaker-warming-serverless-functions-better-with-heterogeneity)
        - [2.INFless: a native serverless system for low-latency, high-throughput inference](#2infless-a-native-serverless-system-for-low-latency-high-throughput-inference)
        - [3.FaaSFlow: enable efficient workflow execution for function-as-a-service](#3faasflow-enable-efficient-workflow-execution-for-function-as-a-service)
        - [4.Serverless computing on heterogeneous computers](#4serverless-computing-on-heterogeneous-computers)
      - [2021](#2021)
        - [1.Nightcore: efficient and scalable serverless computing for latency-sensitive, interactive microservices](#1nightcore-efficient-and-scalable-serverless-computing-for-latency-sensitive-interactive-microservices)
        - [2.FaasCache: keeping serverless computing alive with greedy-dual caching](#2faascache-keeping-serverless-computing-alive-with-greedy-dual-caching)
        - [3.Benchmarking, analysis, and optimization of serverless function snapshots](#3benchmarking-analysis-and-optimization-of-serverless-function-snapshots)
      

# CCFA

## Conference

### ASPLOS

> 摘要截止日期 2022.10.20

#### 2022

> 2022.2.28-3.14
>
> 有专门的关于 serverless 的会议主题

##### 1.IceBreaker: Warming Serverless Functions Better with Heterogeneity 

**摘要：**

无服务器计算是一种新兴的计算模式，它依赖于在预期执行前的 "预热 "函数，以便为用户提供更快、更经济的服务。不幸的是，**预热函数可能是不准确的，并且在预热期间会产生令人望而却步的昂贵成本（即函数保活成本）**。在本文中，**我们介绍了 IceBreaker，这是一种新颖的技术，通过用异构节点（昂贵和便宜）组成系统来减少服务时间和 "保活 "成本。IceBreaker 的做法是，根据函数的时间变化概率，动态地确定在具有成本效益类型的节点来预热函数。通过采用异构性，IceBreaker 允许在相同的成本预算下拥有更多数量的节点，因此可以保活更多数量的函数，并减少高负载时的等待时间**。我们的实际系统评估证实，IceBreaker 使用具有代表性的无服务器应用程序和行业级工作负载跟踪，将整体保持不变的成本降低了 45％，执行时间降低了 27％。IceBreaker 是第一个采用并利用昂贵和便宜节点混合的想法来改善无服务器函数的服务时间和保持成本的技术--为研究人员和从业者开辟了一条在异构服务器上进行无服务器计算的新研究途径。

##### 2.INFless: a native serverless system for low-latency, high-throughput inference

**摘要：**

现代网站越来越依赖机器学习（ML）来提高其业务效率。开发和维护 ML 服务会给开发者带来高昂的成本。虽然无服务器系统是一个很有前途的降低成本的解决方案，但我们**发现目前的通用无服务器系统不能满足 ML 服务的低延迟、高吞吐量的需求。**

虽然简单地 "修补 "通用无服务器系统并不能完全解决这个问题，但我们建议这样的系统应该将推理的特点与无服务器范式天然地结合起来。我们**提出了 INFless，这是第一个针对 ML 领域的无服务器平台。它在 CPU 和加速器之间提供了一个统一的、异构的资源抽象，并利用内置的批处理和非统一的扩展机制实现了高吞吐量。**它还通过协调管理批处理排队时间、执行时间和**冷启动率**支持低延迟。我们使用本地集群测试平台和大规模模拟来评估 INFless。实验结果表明，INFless 在系统吞吐量上优于最先进的系统 2-5 倍，满足了 ML 服务的延时目标。

##### 3.FaaSFlow: enable efficient workflow execution for function-as-a-service 

**摘要：**

无服务器计算（Function-as-a-Service）通过在容器中运行函数（或 Lambda）提供细粒度的资源共享。依赖于数据的函数需要按照预先定义的逻辑进行调用，这就是所谓的**无服务器工作流**。然而，我们的调查显示，传统的基于 master-worker 工作流执行架构在无服务器背景下表现不佳。**master-worker 工作流调度模式导致了一项重大开销，其中函数在主节点中触发并分配给工作节点执行。此外，worker 之间的数据移动也降低了吞吐量。**

为此，我们**提出了一种用于无服务器工作流执行的 worker-side 工作流计划模式**。根据该设计，我们实现了 FaaSFlow，**以便在无服务器环境下实现高效的工作流执行**。**此外，我们提出了一个自适应存储库 FaaStore，它能够在同一节点上的函数之间快速传输数据，而无需通过数据库**。实验结果表明，FaaSFlow 有效地将工作流调度开销平均降低了 74.6%，数据传输开销最多降低了 95%。当网络带宽波动时，FaaSFlow-FaaStore 可以减少 23.0% 的吞吐量下降，并且能够使网络带宽的利用率提高 1.5-4 倍。

##### 4.Serverless computing on heterogeneous computers 

**摘要：**

现有的无服务器计算平台是建立在**同构**计算机基础上的，限制了函数密度，并将无服务器计算限制在有限的场景中。我们介绍**Molecule，这是第一个利用异构计算机的无服务器计算系统**。Molecule 使通用设备（如 Nvidia DPU）和特定领域的加速器（如 FPGA 和 GPU）都能用于无服务器应用，从而显著提高函数密度（高出 50%）和应用性能（高达 34.6 倍）。为了实现这些结果，我们首先提出了 XPU-Shim，这是一个分布式的 Shim，用于弥补底层多操作系统（当使用通用设备时）和我们的无服务器运行时间（即 Molecule）之间的差距。我们进一步介绍了矢量化沙箱，这是一种抽象硬件异构性的沙箱抽象（当使用特定领域的加速器时）。此外，我们还**回顾了关于启动和通信延迟的最先进的无服务器优化**，并克服了在异构计算机上实现这些优化的挑战。我们已经在实际平台上用 Nvidia DPU 和 Xilinx FPGA 实现了 Molecule，并使用基准和实际应用对其进行了评估。

> 研讨会
>
> [vHive 教程及 serverless 讲解](https://www.youtube.com/playlist?list=PLVdxPJaekjWqBsEUwnrYRQCaMqvcDVsBE)

#### 2021 

> 2021.4.19-4.23

##### 1.Nightcore: efficient and scalable serverless computing for latency-sensitive, interactive microservices 

摘要：

微服务架构是一种流行的软件工程方法，用于构建灵活的大规模在线服务。无服务器计算或者函数计算提供了一个简单的无状态函数编程模型，它是实现微服务的无状态 RPC 处理程序的自然基础，是容器化 RPC 服务器的替代方案。但是，**当前的无服务器平台具有毫秒级的运行时开销，使其无法满足现有交互式微服务所需的严格的亚毫秒级延迟目标**。 

我们展示了 **Nightcore，这是一个具有微秒级开销的无服务器函数运行时，可在函数之间提供基于容器的隔离。Nightcore 的设计仔细考虑了具有微秒级开销的各种因素，包括函数请求的调度、通信原语、I/O 的线程模型和并发函数执行。** Nightcore 目前支持用 C/C++、Go、Node.js 和 Python 编写的无服务器函数。我们的评估表明，在运行延迟敏感的交互式微服务时，Nightcore 实现了 1.36–2.93 倍更高的吞吐量和高达 69% 的尾部延迟减少。

##### 2.FaasCache: keeping serverless computing alive with greedy-dual caching 

**摘要：**

函数即服务（也称为无服务器计算）有望彻底改变应用程序使用云资源的方式。但是，由于在开始执行之前初始化其代码和数据依赖关系的开销，函数会遇到冷启动问题。**在函数完成执行后保活函数可以减轻冷启动开销**。Keep-alive 策略必须根据函数的资源和使用特性保持函数处于活动状态，**由于 FaaS 工作负载的多样性，这具有挑战性**。

我们的见解是，keep-alive 类似于缓存。与当前方法相比，**我们受缓存启发的 Greedy-Dual keep-alive 策略可以有效地将冷启动开销减少 3 倍以上。重用距离和命中率曲线等缓存概念也可用于自适应的服务器资源配置**，这可以将 FaaS 提供商对现实世界动态工作负载的资源需求降低 30%。我们在基于 OpenWhisk 的 FaasCache 系统中实施基于缓存的保活和资源配置策略。我们希望我们的缓存类比为未来的 FaaS 工作负载和平台打开了更多原则和优化的保活和资源配置技术的大门。

##### 3.Benchmarking, analysis, and optimization of serverless function snapshots 

**摘要：**

无服务器计算因其高可扩展性和灵活的即用即付计费模式而被迅速采用。在无服务器中，开发人员将他们的服务构建为一组函数，由各种事件（如点击）零星地调用。函数调用的时间间隔变化很大，致使提供者在每次调用时都要启动新的函数实例，从而导致严重的冷启动延迟，降低了用户体验。**为了减少冷启动延迟，业界已转向快照，即在磁盘上存储一个完全启动的函数的镜像**，与从头开始启动函数相比，调用速度更快。

这项工作引入了 **vHive，这是一个用于无服务器实验的开源框架**，旨在使研究人员能够在整个无服务器堆栈中进行研究和创新。使用 vHive，我们描述了一个最先进的基于快照的无服务器基础设施，它基于业界领先的 Containerd 协调框架和 Firecracker 管理程序技术。**我们发现从快照开始的函数的执行时间平均比同一个函数驻留在内存时高 95%。我们表明高延迟归因于频繁的缺页故障**，因为函数的状态一次一页地从磁盘进入客户内存。我们的分析进一步表明，**在同一函数的不同调用中，函数访问的是相同的稳定工作页面集**。通过利用这一洞察，我们**构建了 REAP，这是一种用于无服务器主机的轻量级软件机制，它可以记录函数的客户内存页的稳定工作集，并主动将其从磁盘预取到内存中。**与基线快照相比，REAP 将冷启动延迟平均减少了 3.7 倍。

