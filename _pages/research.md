---
layout: single
title: "Research Projects"
permalink: /research/
author_profile: true
---

Sep. 2020 - Oct. 2021: **ReDCIM and TranCIM. Reconfigurable Digital Computing-in-Memory: Innovative Design Philosophy for AI Chips.**
- A 28nm 29.2TFLOPS/W BF16 and 36.5TOPS/W INT8 Reconfigurable Digital CIM Processor with Unified FP/INT Pipeline and Bitwise in-Memory Booth Multiplication for Cloud Deep Learning Acceleration (**ISSCC'22**)
  - I designed a 28nm Reconfigurable Digital CIM (ReDCIM) chip for cloud AI, with flexible FP/INT support and three features from top to bottom. 
    - ReDCIM is designed on an in-memory alignment-free FP MAC pipeline that interleaves exponent alignment and INT mantissa MAC. Both inputs and weights are pre-aligned to their local maximum exponents, so CIM focuses on only MAC acceleration without complex alignment logic. 
    - A Bitwise in-Memory Booth Multiplication (BM$^2$) architecture is designed with bitwise input Booth encoding in the BM$^2$ controller and partial product recoding in the SRAM-CIM macro, which reduces nearly 50% cycle count and bitwise multiplications. 
    - ReDCIM implements hierarchical and reconfigurable in-memory accumulators to enable flexible support of BF16 (BFloat16)/FP32 and INT8/16 in the same CIM macro.
- A 28nm 15.59$\mu$J/Token Full-Digital Bitline-Transpose CIM-based Sparse Transformer Accelerator with Pipeline/Parallel Reconfigurable Modes (**ISSCC'22**)
  - I designed a 28nm Transformer CIM (TranCIM) chip following the reconfigurable digital CIM design philosophy. There are three features targeting the memory and computation challenges raised by the attention mechanism of Transformer models.
    - TranCIM connects its CIM engines through a reconfigurable streaming network (RSN) with dedicated modes for different layers in Transformer: Pipeline mode for attention layers and parallel mode for fully-connected layers. 
    - TranCIM's SRAM-CIM macro is designed with a bitline-transpose structure to align the directions of input feeding and weight writing. Thus in the QKT-pipeline mode, transposing K is realized without additional storage and buffer access. 
    - TranCIM implements a sparse attention scheduler (SAS) to dynamically configure CIM workload for different sparse attention patterns.
- ReDCIM is the first CIM chip for cloud AI. TranCIM is the first CIM chip for Transformer models.

Apr. 2018 - Aug. 2020: **Evolver, Evolvable AI Chip.**

- [Evolver: A Deep Learning Processor with On-Device Quantization-Voltage-Frequency Tuning](https://ieeexplore.ieee.org/document/9209075) (**JSSC'21**)
  - I designed a 28nm evolvable AI chip (Evolver) with DNN training and reinforcement learning capabilities, to enable intelligence evolution during the chip's long lifetime. This work demonstrates a lifelong learning example of on-device quantization-voltage-frequency (QVF) tuning. Compared with conventional QVF tuning that determines policies offline, Evolver makes optimal customizations for varying local user scenarios. To improve the performance and energy efficiency of both DNN training and inference, we introduce three techniques in the architecture level.
    - Evolver contains a reinforcement learning unit (RLU) that searches QVF polices based on its direct feedbacks. An outlier-skipping scheme is proposed to save unnecessary training for invalid policies under the profiled latency and energy constraints.
    - We exploit the inherent sparsity of feature/error maps in DNN training’s feedforward and backpropagation passes, and design a bidirectional speculation unit (BSU) to capture runtime sparsity and discard zero-output computation, thus reducing training cost. The feedforward speculation also benefits the execution mode.
    - Since the runtime sparsity causes time-varying workload parallelism that harms performance and efficiency, we design a reconfigurable computing engine (RCE) with an online configuration compiler (OCC) for Evolver, in order to dynamically reconfigure dataflow parallelism to match workload parallelism.
  - Evolver was nominated for [2021 Top-10 Research in China’s Semiconductors](https://mp.weixin.qq.com/s/Sad4Kc9lP8XW9vebdt7KaA).

Feb. 2017 - Mar. 2018: **RANA, DNN Accelerator with High-Density Memory and Software-Hardware Co-design.**

- [RANA: Towards Efficient Neural Acceleration with Refresh-Optimized Embedded DRAM](https://ieeexplore.ieee.org/document/8416839/) (**ISCA'18**) 
  - I designed a retention-aware neural acceleration (RANA) framework, which strengthens DNN accelerators with refresh-optimized eDRAM to save total system energy. RANA includes three techniques from the training, scheduling, architecture levels respectively.
    - **Training Level**: A retention-aware training method is proposed to improve eDRAM's tolerable retention time with no accuracy loss. Bit-level retention errors are injected during training, so the network' s tolerance to retention failures is improved. A higher tolerable failure rate leads to longer tolerable retention time, so more refresh can be removed.
    - **Scheduling Level**: A system energy consumption model is built in consideration of computing energy, on-chip buffer access energy, refresh energy and off-chip memory access energy. RANA schedules networks in a hybrid computation pattern based on this model. Each layer is assigned with the computation pattern that costs the lowest energy.
    - **Architecture Level**: RANA independently disables refresh to eDRAM banks based on their storing data's lifetime, saving more refresh energy. A programmable eDRAM controller is proposed to enable the above fine-grained refresh controls.
  - RANA was the **only** work first-authored by a Chinese research team in ISCA'18, and covered by [Tsinghua University News](https://www.tsinghua.edu.cn/info/1175/19449.htm) and [AI Tech Talk](https://www.leiphone.com/news/201806/wFQ2Sc52Utikcl8D.html).

Jan. 2016 - Present: [**Neural Networks on Silicon.**](https://github.com/fengbintu/Neural-Networks-on-Silicon)

- I'm collecting works on neural network accelerators and related topics, in a GitHub project named [Neural Networks on Silicon](https://github.com/fengbintu/Neural-Networks-on-Silicon). It has attracted many researchers all around the world.

Sep. 2015 - Oct. 2016: **DNA and Thinker, Reconfigurable Architecture for DNN Acceleration.**

- [Deep Convolutional Neural Network Architecture with Reconfigurable Computation Patterns](http://ieeexplore.ieee.org/document/7898402/) (**TVLSI popular paper. No.5/2/6/8/8 Downloaded Manuscripts in 2017~2021: 6 Times Monthly No.1 since Sep. 2017.**)
  - I designed a deep convolutional neural network accelerator (DNA) targeting flexible and efficient CNN acceleration. This is the first work to assign Input/Output/Weight Reuse to different layers of a CNN, which optimizes system-level energy consumption based on different CONV parameters. DNA has two main features, in the architecture level and scheduling leverl, respectively.
    - A 4-level CONV engine is designed to to support different tiling parameters for higher resource utilization and performance.
    - A layer-based scheduling framework is proposed to optimize both system-level energy efficiency and performance.
- [A High Energy Efficient Reconfigurable Hybrid Neural Network Processor for Deep Learning Applications](http://ieeexplore.ieee.org/document/8207783/) (**JSSC'18**) 
  - A reconfigurable multi-modal neural network processor (Thinker) was fabricated based on the DNA architecture, supporting CNN, RNN, and FCN. 
  - The Thinker chip was exhibited at the [2016 National Mass Innovation and Entrepreneurship Week](https://www.tsinghua.edu.cn/info/1173/18061.htm), as a representative work from Tsinghua University. The Thinker chip was highly praised by Chinese Premier Li Keqiang, and featured by Yang Lan One on One, [AI Tech Talk](https://www.leiphone.com/news/201705/8sB0WHz6D70J7NAy.html) and [MIT Technology Review](https://www.technologyreview.com/s/609954/china-wants-to-make-the-chips-that-will-add-ai-to-any-gadget/?from=timeline&isappinstalled=0). It won the [ISLPED'17 Design Contest Award](http://islped.org/2017/index.php), which was [the first time for a China Mainland team to win the award](https://www.tsinghua.edu.cn/info/1175/19744.htm).

Oct. 2013 - Oct. 2014: **RNA, Reconfigurable Architecture for Neural Approximation.**

- [Reconfigurable Architecture for Neural Approximation in Multimedia Computing](http://ieeexplore.ieee.org/document/8307081/) (**TCSVT'19**)
    - I designed a reconfigurable neural accelerator (RNA) that can be reconfigured for different neural networks. RNA targets approximate computing in multiple application domains.
