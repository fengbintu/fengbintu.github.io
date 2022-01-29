---
layout: single
title: "Research Projects"
permalink: /research/
author_profile: true
---

Sep. 2020 - Oct. 2021: **Processing-in-Memory and Modern NN Acceleration**
* I designed two SRAM-based Processing-in-Memory chips for modern NN acceleration. The two chips were fabricated in the TSMC 28nm technology and recently accepted by ISSCC'22. More information will be released soon.

Apr. 2018 - Aug. 2020: [**Evolver**](https://ieeexplore.ieee.org/document/9209075)

* I designed a deep learning processor (Evolver) with DNN training and reinforcement learning capabilities, to enable intelligence evolution during the chip's long lifetime. This work demonstrates a lifelong learning example of on-device quantization-voltage-frequency (QVF) tuning. Compared with conventional QVF tuning that determines policies offline, Evolver makes optimal customizations for varying local user scenarios. To improve the performance and energy efficiency of both DNN training and inference, we introduce three techniques in the architecture level: 
  - Evolver contains a reinforcement learning unit (RLU) that searches QVF polices based on its direct feedbacks. An outlier-skipping scheme is proposed to save unnecessary training for invalid policies under the profiled latency and energy constraints.
  - We exploit the inherent sparsity of feature/error maps in DNN training’s feedforward and backpropagation passes, and design a bidirectional speculation unit (BSU) to capture runtime sparsity and discard zero-output computation, thus reducing training cost. The feedforward speculation also benefits the execution mode.
  - Since the runtime sparsity causes time-varying workload parallelism that harms performance and efficiency, we design a reconfigurable computing engine (RCE) with an online configuration compiler (OCC) for Evolver, in order to dynamically reconfigure dataflow parallelism to match workload parallelism.

Feb. 2017 - Mar. 2018: [**RANA**](https://ieeexplore.ieee.org/abstract/document/8416839/)

* I designed a Retention-Aware Neural Acceleration (RANA) framework that strengthens current DNN accelerators with refresh-optimized eDRAM to save total system energy, through techniques from training, scheduling and architecture levels. RANA was the **only** work first-authored by a Chinese research team in ISCA'18, and covered by [Tsinghua University News](https://www.tsinghua.edu.cn/info/1175/19449.htm) and [AI Tech Talk](https://www.leiphone.com/news/201806/wFQ2Sc52Utikcl8D.html). RANA includes three levels of techniques: 
  - **Training Level**: A retention-aware training method is proposed to improve eDRAM's tolerable retention time with no accuracy loss. Bit-level retention errors are injected during training, so the network' s tolerance to retention failures is improved. A higher tolerable failure rate leads to longer tolerable retention time, so more refresh can be removed.
  - **Scheduling Level**: A system energy consumption model is built in consideration of computing energy, on-chip buffer access energy, refresh energy and off-chip memory access energy. RANA schedules networks in a hybrid computation pattern based on this model. Each layer is assigned with the computation pattern that costs the lowest energy.
  - **Architecture Level**: RANA independently disables refresh to eDRAM banks based on their storing data's lifetime, saving more refresh energy. A programmable eDRAM controller is proposed to enable the above fine-grained refresh controls.

Jan. 2016 - Present: [**Neural Networks on Silicon**](https://github.com/fengbintu/Neural-Networks-on-Silicon)

* I'm collecting works on neural network accelerators and related topics, in a GitHub project named [Neural Networks on Silicon](https://github.com/fengbintu/Neural-Networks-on-Silicon). It has attracted many researchers all around the world.

Sep. 2015 - Oct. 2016: [**DNA**](http://ieeexplore.ieee.org/document/7898402/) and [**Thinker**](http://ieeexplore.ieee.org/document/8207783/)

* I design a deep convolutional neural network accelerator (DNA) targeting flexible and efficient CNN acceleration. 
  - This is the first work to assign Input/Output/Weight Reuse to different layers of a CNN, which optimizes system-level energy consumption based on different CONV parameters.
  - A 4-level CONV engine is designed to to support different tiling parameters for higher resource utilization and performance.
  - A layer-based scheduling framework is proposed to optimize both system-level energy efficiency and performance.
* A reconfigurable multi-modal neural network processor (Thinker) was fabricated based on the DNA architecture. The Thinker chip was exhibited at the [2016 National Mass Innovation and Entrepreneurship Week](https://www.tsinghua.edu.cn/info/1173/18061.htm), as a representative work from Tsinghua University. The Thinker chip was highly praised by Chinese Premier Li Keqiang, and featured by Yang Lan One on One, [AI Tech Talk](https://www.leiphone.com/news/201705/8sB0WHz6D70J7NAy.html) and [MIT Technology Review](https://www.technologyreview.com/s/609954/china-wants-to-make-the-chips-that-will-add-ai-to-any-gadget/?from=timeline&isappinstalled=0). It won the [ISLPED'17 Design Contest Award](http://islped.org/2017/index.php), which was [the first time for a Chinese Mainland team to win the award](https://www.tsinghua.edu.cn/info/1175/19744.htm).

Mar. 2015 - Dec. 2016: **Image/Video Encoder Based on RNA**

* I designed an image/video encoding system based on my previous design RNA. The system can online switch to an image encoder or video encoder, by reconfiguring the processing core RNA.

Oct. 2013 - Oct. 2014: [**RNA**](http://ieeexplore.ieee.org/document/8307081/)

* I designed a reconfigurable neural accelerator (RNA) that can be configured for different neural networks. RNA targets approximate computing in multiple application domains.
