# About Me
My name is Fengbin Tu. I'm currently working with Prof. [Yuan Xie](https://www.ece.ucsb.edu/~yuanxie/index.html), as a postdoctoral researcher at the Scalable Energy-efficient Architecture Lab (SEAL), Electrical and Computer Engineering Department, UCSB. Before joining UCSB, I received my Ph.D. degree from the Institute of Microelectronics, Tsinghua University. My dissertation is entitled "[**Architecture Design and Memory Optimization for Neural Network Accelerators**](http://gb.oversea.cnki.net/kcms/detail/detail.aspx?recid=&FileName=1020828815.nh&DbName=CDFDTEMP&DbCode=CDFD&uid=WEEvREcwSlJHSldSdmVqeVpQU2FqamhKMTZ1TXFRUzdVYm9XaVJjQ1pkVT0=$9A4hF_YAuvQ5obgVAqNKPCYcEjKensW4IQMovwHtwkF4VYPoHbKxJw!!)", and won the Tsinghua Excellent Dissertation Award, advised by Prof. Shaojun Wei and Prof. Shouyi Yin. 

In 2020, I designed a deep learning processor ([Evolver](https://ieeexplore.ieee.org/document/9209075)) with DNN training and reinforcement learning capabilities. Evolver goes beyond my previous DNN inference chip Thinker, representing a step towards lifelong learning. 

In 2018, I designed a Retention-Aware Neural Acceleration (RANA) framework that strengthens current DNN accelerators with refresh-optimized eDRAM to save total system energy, through techniques from training, scheduling and architecture levels. RANA was the **only** work first-authored by a Chinese research team in ISCA'18, and covered by [Tsinghua University News](http://news.tsinghua.edu.cn/publish/thunewsen/9671/2018/20180613125238640581215/20180613125238640581215_.html) and [AI Tech Talk](https://www.leiphone.com/news/201806/wFQ2Sc52Utikcl8D.html).

In 2016, a reconfigurable multi-modal neural network processor ([Thinker](http://ieeexplore.ieee.org/document/8207783/)) was designed based on my [DNA](http://ieeexplore.ieee.org/document/7898402/) architecture. The Thinker chip was exhibited at the [2016 National Mass Innovation and Entrepreneurship Week](http://news.tsinghua.edu.cn/publish/thunews/9648/2016/20161013102253491194453/20161013102253491194453_.html), as a representative work from Tsinghua University. The Thinker chip was highly praised by Chinese Premier Li Keqiang, and featured by [Yang Lan One on One](http://www.iqiyi.com/v_19rr77vmeo.html?wx_uid1=wxidoG0a9jsItpryB9soI-lGgUuUtvlc&wx_uid2=wxidoG0a9jsItpryB9soI-lGgUuUtvlc), [AI Tech Talk](https://www.leiphone.com/news/201705/8sB0WHz6D70J7NAy.html) and [MIT Technology Review](https://www.technologyreview.com/s/609954/china-wants-to-make-the-chips-that-will-add-ai-to-any-gadget/?from=timeline&isappinstalled=0). It won the [ISLPED'17 Design Contest Award](http://islped.org/2017/index.php), which was [the first time for a Chinese Mainland team to win the award](http://news.tsinghua.edu.cn/publish/thunews/10303/2017/20170809193415062503521/20170809193415062503521_.html).

This is an exciting field where fresh ideas come out every day, so I'm maintaining a project named [Neural Networks on Silicon](https://github.com/fengbintu/Neural-Networks-on-Silicon), to collect works that interest me and make comments on them.

# Research Interests
Computer Architecture, Deep Learning, VLSI Design, Approximate Computing, Reconfigurable Computing

# Professional Experience
Oct. 2019 - Present: **University of California, Santa Barbara (UCSB)**

* Postdoctoral researcher, working with Prof. [Yuan Xie](https://www.ece.ucsb.edu/~yuanxie/index.html)

# Education
Sep. 2013 - Jul. 2019: **Tsinghua University (THU)**

* Dissertation: Architecture Design and Memory Optimization for Neural Network Accelerators
  - Tsinghua Excellent Dissertation Award
* GPA 3.8/4.0, Rank 2/20 in the Institute of Microelectronics 
* Ph.D. in Electronic Science and Technology

Sep. 2009 - Jun. 2013: **Beijing University of Posts and Telecommunications (BUPT)**

* GPA 3.9/4.0, Rank 1/255 in the School of Electronic Engineering
* B.S. in Electronic Science and Technology 

# Project Experience
Apr. 2018 - Aug. 2020: [**Evolver**](https://ieeexplore.ieee.org/document/9209075)

* I design a deep learning processor (Evolver) with DNN training and reinforcement learning capabilities, to enable intelligence evolution during the chip's long lifetime. This work demonstrates a lifelong learning example of on-device quantization-voltage-frequency (QVF) tuning. Compared with conventional QVF tuning that determines policies offline, Evolver makes optimal customizations for varying local user scenarios. To improve the performance and energy efficiency of both DNN training and inference, we introduce three techniques in the architecture level: 
  - Evolver contains a reinforcement learning unit (RLU) that searches QVF polices based on its direct feedbacks. An outlier-skipping scheme is proposed to save unnecessary training for invalid policies under the profiled latency and energy constraints.
  - We exploit the inherent sparsity of feature/error maps in DNN training’s feedforward and backpropagation passes, and design a bidirectional speculation unit (BSU) to capture runtime sparsity and discard zero-output computation, thus reducing training cost. The feedforward speculation also benefits the execution mode.
  - Since the runtime sparsity causes time-varying workload parallelism that harms performance and efficiency, we design a reconfigurable computing engine (RCE) with an online configuration compiler (OCC) for Evolver, in order to dynamically reconfigure dataflow parallelism to match workload parallelism.

Feb. 2017 - Mar. 2018: [**RANA**](https://ieeexplore.ieee.org/abstract/document/8416839/)

* I design a retention-aware neural acceleration (RANA) framework that strengthens DNN accelerators with refresh-optimized eDRAM to save total system energy. RANA includes three levels of techniques: 
  - **Training Level**: A retention-aware training method is proposed to improve eDRAM's tolerable retention time with no accuracy loss. Bit-level retention errors are injected during training, so the network' s tolerance to retention failures is improved. A higher tolerable failure rate leads to longer tolerable retention time, so more refresh can be removed.
  - **Scheduling Level**: A system energy consumption model is built in consideration of computing energy, on-chip buffer access energy, refresh energy and off-chip memory access energy. RANA schedules networks in a hybrid computation pattern based on this model. Each layer is assigned with the computation pattern that costs the lowest energy.
  - **Architecture Level**: RANA independently disables refresh to eDRAM banks based on their storing data's lifetime, saving more refresh energy. A programmable eDRAM controller is proposed to enable the above fine-grained refresh controls.
* RANA was the **only** work first-authored by a Chinese research team in ISCA'18.

Jan. 2016 - Present: [**Neural Networks on Silicon**](https://github.com/fengbintu/Neural-Networks-on-Silicon)

* I'm collecting works on neural network accelerators and related topics, in a GitHub project named [Neural Networks on Silicon](https://github.com/fengbintu/Neural-Networks-on-Silicon). It has attracted many researchers all around the world.

Sep. 2015 - Oct. 2016: [**DNA**](http://ieeexplore.ieee.org/document/7898402/) and [**Thinker**](http://ieeexplore.ieee.org/document/8207783/)

* I design a deep convolutional neural network accelerator (DNA) targeting flexible and efficient CNN acceleration. 
  - This is the first work to assign Input/Output/Weight Reuse to different layers of a CNN, which optimizes system-level energy consumption based on different CONV parameters.
  - A 4-level CONV engine is designed to to support different tiling parameters for higher resource utilization and performance.
  - A layer-based scheduling framework is proposed to optimize both system-level energy efficiency and performance.
* A reconfigurable multi-modal neural network processor (Thinker) is fabricated based on the DNA architecture.

Mar. 2015 - Dec. 2016: **Image/Video Encoder Based on RNA**

* I design an image/video encoding system based on my previous design RNA. The system can online switch to an image encoder or video encoder, by reconfiguring the processing core RNA.

Oct. 2013 - Oct. 2014: [**RNA**](http://ieeexplore.ieee.org/document/8307081/)

* I design a reconfigurable neural accelerator (RNA) that can be configured for different neural networks. RNA targets approximate computing in multiple application domains.

# Selected Publications
Journal Papers
* **[JSSC'21]** **F. Tu**, W. Wu, Y. Wang, H. Chen, F. Xiong, M. Shi, N. Li, J. Deng, T. Chen, L. Liu, S. Wei, Y. Xie, S. Yin, "[Evolver: A Deep Learning Processor with On-Device Quantization-Voltage-Frequency Tuning](https://ieeexplore.ieee.org/document/9209075)," IEEE Journal of Solid-State Circuits (JSSC), 2021.
* **[TCSVT'18]** **F. Tu**, S. Yin, P. Ouyang, L. Liu, S. Wei, "[Reconfigurable Architecture for Neural Approximation in Multimedia Computing](http://ieeexplore.ieee.org/document/8307081/)," IEEE Transactions on Circuits and Systems for Video Technology (TCSVT), 2018.
* **[JSSC'18]** S. Yin, P. Ouyang, S. Tang, **F. Tu**, X. Li, S. Zheng, T. Lu, J. Gu, L. Liu, S. Wei, "[A High Energy Efficient Reconfigurable Hybrid Neural Network Processor for Deep Learning Applications](http://ieeexplore.ieee.org/document/8207783/)," IEEE Journal of Solid-State Circuits (JSSC), 2018. (**The 1st Student Author**)
* **[TVLSI'17]** **F. Tu**, S. Yin, P. Ouyang, S. Tang, L. Liu, S. Wei, "[Deep Convolutional Neural Network Architecture with Reconfigurable Computation Patterns](http://ieeexplore.ieee.org/document/7898402/)," IEEE Transactions on Very Large Scale Integration Systems (TVLSI), 2017. (**TVLSI No.5/2/6 Downloaded Manuscripts in 2017/2018/2019: 6 Times Monthly No.1 since Sep. 2017.**)

Conference Papers
* **[HotChips'20]** **F. Tu**, W. Wu, Y. Wang, H. Chen, F. Xiong, M. Shi, N. Li, J. Deng, T. Chen, L. Liu, S. Wei, S. Yin, "[ELearn: Edge Learning Processor with Bidirectional Speculation and Sparsity & Mixed-Precision aware Dataflow Parallelism Reconfiguration](https://ieeexplore.ieee.org/document/9250188)," Hot Chips, Virtual, 2020. 
* **[ISCA'18]** **F. Tu**, W. Wu, S. Yin, L. Liu, S. Wei, "[RANA: Towards Efficient Neural Acceleration with Refresh-Optimized Embedded DRAM](https://ieeexplore.ieee.org/abstract/document/8416839/)," International Symposium on Computer Architecture (ISCA), Los Angeles, USA, 2018. (**Acceptance Rate: 16.9% = 64/378**)
* **[VLSI'17]** S. Yin, P. Ouyang, S. Tang, **F. Tu**, L. Liu, S. Wei, "A 1.06-to-5.09 TOPS/W Reconfigurable Hybrid-Neural-Network Processor	for Deep Learning Applications," Symposia on VLSI Technology and Circuits (VLSI Symposia), Kyoto, Japan, 2017. (**The 1st Student Author**)
* **[ISSCC-SRP'17]** **F. Tu**, S. Yin, P. Ouyang, S. Tang, L. Liu, S. Wei, "A Reconfigurable Multi-modal Neural Processor for Cognitive Intelligence Applications," Presentation at the ISSCC Student Research Preview Session (ISSCC-SRP), San Francisco, USA, 2017. (**Acceptance Rate < 25%**)
* **[DATE'15]** **F. Tu**, S. Yin, P. Ouyang, L. Liu, S. Wei, “RNA: A Reconfigurable Architecture for Hardware Neural Acceleration," Design, Automation and Test in Europe Conference (DATE), Grenoble, France, 2015. (**Acceptance Rate: 22%**)
* **[ISCAS'15]** **F. Tu**, S. Yin, P. Ouyang, L. Liu, S. Wei, “Neural Approximating Architecture  Targeting Multiple Application Domains," IEEE International Symposium on Circuits and Systems (ISCAS), Lisbon, Portugal, 2015.

Featured Co-authored Papers
* **[DAC'21]** X. Lin, L. Sun, **F. Tu**, L. Liu, X. Li, S. Wei, S. Yin, "ADROIT: An Adaptive Dynamic Refresh Optimization Framework for DRAM Power Saving in DNN Training," Design Automation Conference (DAC), Virtual, 2021.
* **[MICRO'20]** L. Liu, Z. Qu, L. Deng, **F. Tu**, S. Li, X. Hu, Z. Gu, Y. Ding, Y. Xie, "DUET: Boosting Deep Neural Network Efficiency on Dual-Module Architecture," IEEE/ACM International Symposium on Microarchitecture (MICRO), Virtual, 2020. (**Acceptance Rate: 15.6% = 66/422**)
* **[DAC'20]** F. Xiong, **F. Tu**, M. Shi, Y. Wang, L. Liu, S. Wei, S. Yin, "STC: Significance-Aware Transform-Based Codec Framework for External Memory Access Reduction," Design Automation Conference (DAC), San Francisco, USA, 2020. (Co-advisor)
* **[ISVLSI'19]** F. Xiong, **F. Tu**, S. Yin, S. Wei, "Towards Efficient Compact Network Training on Edge-Devices," IEEE Computer Society Annual Symposium on VLSI (ISVLSI), Miami, USA, 2019. (**Invited Paper**, Co-advisor)
* **[TPDS'18]** S. Yin, S. Tang, X. Lin, P. Ouyang, **F. Tu**, L. Liu, J. Zhao, C. Xu, S. Li, Y. Xie, S. Wei, "Parana: A Parallel Neural Architecture Considering Thermal Problem of 3D Stacked Memory," IEEE Transactions on Parallel and Distributed Systems (TPDS), 2018. 
* **[TCAD'18]** J. Yan, S. Yin, **F. Tu**, L. Liu, S. Wei, "GNA: Reconfigurable and Efficient Architecture for Generative Network Acceleration," IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (TCAD), 2018. (Co-advisor)
* **[TCAD'18]** S. Yin, S. Tang, X. Lin, P. Ouyang, **F. Tu**, L. Liu, S. Wei, "A High Throughput
Acceleration for Hybrid Neural Networks with Efficient Resource Management on FPGA," IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (TCAD), 2018.
* **[DAC'18]** X. Lin, S. Yin, **F. Tu**, L. Liu, X. Li, S. Wei, "LCP: A Layer Clusters Paralleling Mapping Method for Accelerating Inception and Residual Networks on FPGA," Design Automation Conference (DAC), San Francisco, USA, 2018. (**Acceptance Rate: 24.3%**)

# Talks

From Thinker to Evolver: Towards Evolvable Intelligent Hardware
* Biren Technology, Online, Feb. 2021.

Architecture Design and Memory Optimization for Neural Network Accelerators
* Dissertation talk at Tsinghua University, Beijing, China, Jul. 2019.
* 601 Talk, Beijing, China, Jul. 2019.

RANA: Towards Efficient Neural Acceleration with Refresh-Optimized Embedded DRAM
* Conference talk at ISCA, Los Angeles, USA, Jun. 2018. 
* Lightning talk for ISCA, [Online](https://www.youtube.com/watch?v=QmtDP13oXFE&list=PL_i_ACawvXe6jchq9RgA0lOL42EeVA7H4&t=33s&index=5), Jun. 2018.
* Department of Electronic Engineering, Tsinghua University, Beijing, China, Jun. 2018.
* Intel Labs China, Beijing, China, Aug. 2018.
* Lam Research Technical Symposium, Beijing, China, Sep. 2018.

Thinker: A Reconfigurable Hybrid Neural Network Processor for Deep Learning Applications
* Conference talk at ISLPED, Taipei, Jul. 2017.
* Tsinghua-ROHM International Forum of Industry-Academia (TRIFIA), Beijing, China, May 2018.

DNA: Deep Convolutional Neural Network Architecture with Reconfigurable Computation Patterns
* Conference talk at ISSCC, San Francisco, USA, Feb. 2017.
* THU Ph.D. Student Forum, Beijing, China, Oct. 2016.
* Deephi Tech, Beijing, China, Apr. 2017. 
* AI Tech Talk, [Online](https://v.qq.com/x/page/r0504zxvl3j.html) [[Text](https://www.leiphone.com/news/201705/8sB0WHz6D70J7NAy.html)], May 2017.
* Tsinghua-ROHM International Forum of Industry-Academia (TRIFIA), Beijing, China, May 2017.
* Future Chip Forum, Beijing, China, Jun. 2017.
* Momenta, Beijing, China, Aug. 2017.

# Honors and Awards
* Beijing Outstanding Graduate (2013, 2019)
* THU Excellent Dissertation Award (2019)
* THU Outstanding Student Scholarship (2016, 2018)
* THU DengFeng Fellowship (2015, 2018)
* IME Outstanding Young Researcher Award (2018)
* National Scholarship for Ph.D. Students (2017)
* ISLPED'17 Design Contest Winner (2017)
* THU Outstanding Postgraduate Assistant (2016)
* ICFC Fellowship for Outstanding Ph.D. Students (2016)
* Lam Research Scholarship (2015)
* Excellent Paper Award of THU Ph.D. Student Forum (2015)
* National Scholarship for Undergraduate Students (2010, 2011, 2012)
* BUPT Merit Student (2010, 2011, 2012) 

# Book
* S. Yin, **F. Tu**, D. Zhu, S. Wei, "Deep Learning Chip Design," Science Press, 2020.

# Service and Activities
* 2019 - Present: Reviewer, IEEE Transactions on Computer-Aided Design of Integrated Circuits and Systems (TCAD)

# Contact
Address: Ellison Hall 1804, UCSB, Santa Barbara, California, USA

Email1: strcat(last_name, "fengbin") at gmail dot com

Email2: strcat("fengbin", last_name) at ucsb dot edu

![At Cabo da Roca, May, 2015](./portrait.jpg)
At Cabo da Roca, May, 2015.

"Aqui, onde a terra se acaba e o mar começa..." — Luís de Camões, *Os Lusíadas*
