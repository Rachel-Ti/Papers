# Papers

Here are some useful papers about serverless computing.And we look forward to your discussion and exploration with us!

We have simply divided the papers into the following categories for easy selective reading.


## Review（综述型）
综述型论文是对某一专题、某一领域的历史背景、前人工作、争论焦点、研究现状与发展前景等方面，以作者自己的观点写成的严谨而系统的评论性、资料性的论文。会引用某个领域50～100篇（甚至更多）文献参考资料，来辨明其中的关系、矛盾、差距及不一致性，并建议解决问题的后续步骤。该类型论文不要求作者对其研究发现进行阐述，因此这类论文一般在项目初期通过大量的文献资料研究进行撰写。


- **Cloud Programming Simplified: A Berkeley View on Serverless Computing**
  
  > [本文](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2019/EECS-2019-3.pdf)是Berkeley于2019年发表在 _Journal Computing Research Repository (CoRR)_ 上的一篇文章。
  
  论文首先简要回顾了云计算的历史，包括 2009 年伯克利云计算观点论文的预测，然后解释了无服务器计算的动机，描述了一些挑战当前无服务器计算的应用，最后列出了无服务器计算实现其全部潜力的必要障碍和研究机会。正如 2009 年的论文指出了云计算的挑战并预测它们将被解决，云应用将加速，我们预测这些问题是可以解决的，无服务器计算将增长到主导未来云计算的发展。
  
- **Serverless Computing: State-of-the-Art, Challenges and Opportunities**
  
  > IEEE Transactions on Services Computing（2022）
  
  [本文](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9756233)的研究机构：Cloud Center | Center for Cloud Computing | Center for Cloud Computing Research | Faculty of Science and Technology
  
  **摘要**：无服务器计算正因其轻量级和简单的管理而越来越受欢迎。它通过将计算单元的粒度降低到函数级别来实现这些优点。具体来说，无服务器计算允许用户专注于函数本身，而将其他繁琐的管理和调度问题留给平台提供商，后者负责在高性能调度和低资源成本之间取得平衡。在本文中，我们对无服务器计算进行了全面的调查，特别关注其基础架构特性。通过这种方式，我们确定了一些现有挑战，并分析了相关的尖端解决方案。利用这些结果，我们进一步研究了一些典型的开源框架，并研究了它们如何解决确定的挑战。鉴于无服务器计算的巨大优势，预计其部署将主导未来的云平台。因此，我们还看到了一些有待未来进一步探索的有前景的研究机会。我们希望本文的工作能够激发那些从事相关领域的研究人员和实践者，让他们认识到无服务器计算的重要性，从而涉足这个有前景的领域，为它的发展做出巨大贡献。
  
## Analytic（分析型）
分析型论文主要由分析构成，可以是分析数据，或者分析模型等等。

- **Let's Trace It: Fine-Grained Serverless Benchmarking using Synchronous and Asynchronous Orchestrated Applications**
  
  > [本文](https://arxiv.org/pdf/2205.07696.pdf)是存储在 _arXiv_ · Distributed, Parallel, and Cluster Computing（2022）上的一篇文章。
  
  **摘要**：要使无服务器计算广泛适用，需要详细了解性能。尽管现有的基准测试方法存在，但它们仅报告粗略的结果，不使用分布式跟踪，不考虑异步应用程序，并且对（根本原因）分析的能力有限。为解决这个差距，我们设计并实现了 ServiBench，一个无服务器基准测试套件。我们对 AWS 环境中的服务器端应用性能进行了全面的**白盒分析**。ServiBench (i) 利用同步和异步的无服务器应用程序，代表生产使用情况，(ii) 扩展云提供商数据以生成现实的负载，(iii) 进行全面的端到端实验，以捕获应用程序级别的性能，(iv) 使用基于（分布式）无服务器跟踪的新颖方法分析结果，(v) 支持全面的无服务器性能分析。通过 ServiBench，我们对 AWS 进行了全面的实验，涵盖了五个常见的性能因素：**中位数延迟、冷启动、尾延迟、可扩展性和动态工作负载**。我们发现，无服务器应用程序的中位数端到端延迟通常不是由函数计算而是由外部服务调用、编排或基于触发器的协调所主导。我们根据公平原则发布收集的实验数据，并将 ServiBench 作为一个经过测试的可扩展的**开源**工具发布。
  
- 

## Methods（方法型）
方法型论文旨在展示一种新的实验方法、测试方法或者流程，对结果不做过多阐述。其架构和篇幅与研究型论文相似。尽管结果不是这类论文的核心部分，但大部分期刊仍会要求提供结果相关的数据样本。
