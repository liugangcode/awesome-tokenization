# Awesome Foundation Model Tokenization

<!-- A collection for **What Should Count as a Token?**, a comprehensive study of tokenization and data representation across foundation models and scientific data. -->

The collection tracks methods that form, select, merge, quantize, parse, or study model units/tokens. It separates the tokenizer from the foundation model that consumes its output. 

The current release contains 361 literature records and 81 frontier-lab or public models.

<!-- Cutoff: September 6, 2026. -->

## Contents ([Interactive Explorer](https://liugangcode.github.io/awesome-tokenization))

- [0. Cross-Cutting Foundations, Surveys, and Evaluation](#0-cross-cutting-foundations-surveys-and-evaluation)
- [1.1 Text and Code](#11-text-and-code)
- [1.2 Images and Video](#12-images-and-video)
- [1.3 Audio and Speech](#13-audio-and-speech)
- [1.4 Point Clouds and Three-Dimensional Structure](#14-point-clouds-and-three-dimensional-structure)
- [1.5 Graphs and Tables](#15-graphs-and-tables)
- [1.6 Time Series, Physical Fields, and Latent World States](#16-time-series-physical-fields-and-latent-world-states)
- [1.7 Robot Actions and Embodied Trajectory](#17-robot-actions-and-embodied-trajectory)
- [1.8 Multimodal Token Systems](#18-multimodal-token-systems)
- [2.1 DNA and RNA](#21-dna-and-rna)
- [2.2 Proteins and Peptides](#22-proteins-and-peptides)
- [2.3 Molecules and Reactions](#23-molecules-and-reactions)
- [2.4 Crystals, Materials, and Polymers](#24-crystals-materials-and-polymers)
- [2.5 Spectra and Microscopy](#25-spectra-and-microscopy)
- [2.6 Medical Imaging and Digital Pathology](#26-medical-imaging-and-digital-pathology)
- [2.7 Omics and Cells](#27-omics-and-cells)
- [2.8 Physical Fields and Simulations](#28-physical-fields-and-simulations)
- [2.9 Earth System Observations](#29-earth-system-observations)
- [Public Hugging Face Models](#public-hugging-face-models)
- [3. Theoretical and Method Foundations for Future Tokenizers](#3-theoretical-and-method-foundations-for-future-tokenizers)
- [Contributing](#contributing)

## 0. Cross-Cutting Foundations, Surveys, and Evaluation

- 1935\. George Kingsley Zipf. [The Psycho-Biology of Language: An Introduction to Dynamic Philology](https://mitpress.mit.edu/9780262740029/the-psycho-biology-of-language/). *Houghton Mifflin*.
- 1948\. Claude E. Shannon. [A Mathematical Theory of Communication](https://doi.org/10.1002/j.1538-7305.1948.tb01338.x). *Bell System Technical Journal*.
- 1951\. Claude E. Shannon. [Prediction and Entropy of Printed English](https://doi.org/10.1002/j.1538-7305.1951.tb01366.x). *Bell System Technical Journal*.
- 1952\. David A. Huffman. [A Method for the Construction of Minimum-Redundancy Codes](https://doi.org/10.1109/JRPROC.1952.273898). *Proceedings of the IRE*.
- 1960\. Joel Max. [Quantizing for Minimum Distortion](https://doi.org/10.1109/TIT.1960.1057548). *IRE Transactions on Information Theory*.
- 1976\. Abraham Lempel and Jacob Ziv. [On the Complexity of Finite Sequences](https://doi.org/10.1109/TIT.1976.1055501). *IEEE Transactions on Information Theory*.
- 1977\. Jacob Ziv and Abraham Lempel. [A Universal Algorithm for Sequential Data Compression](https://doi.org/10.1109/TIT.1977.1055714). *IEEE Transactions on Information Theory*.
- 1982\. Stuart P. Lloyd. [Least Squares Quantization in PCM](https://doi.org/10.1109/TIT.1982.1056489). *IEEE Transactions on Information Theory*.
- 1982\. Teuvo Kohonen. [Self-Organized Formation of Topologically Correct Feature Maps](https://doi.org/10.1007/BF00337288). *Biological Cybernetics*.
- 1994\. Philip Gage. [A New Algorithm for Data Compression](https://www.derczynski.com/papers/archive/BPE_Gage.pdf). *C Users Journal*.
- 1997\. Craig G. Nevill-Manning and Ian H. Witten. [Identifying Hierarchical Structure in Sequences: A Linear-Time Algorithm](https://doi.org/10.1613/jair.374). *Journal of Artificial Intelligence Research*.
- 1998\. Robert M. Gray and David L. Neuhoff. [Quantization](https://doi.org/10.1109/5.720250). *IEEE Transactions on Information Theory*.
- 2000\. N. Jesper Larsson and Alistair Moffat. [Off-line Dictionary-Based Compression](https://doi.org/10.1109/5.892708). *Proceedings of the IEEE*.
- 2016\. E. Jang, S. Gu, et al. [Categorical reparameterization with gumbel-softmax](https://arxiv.org/abs/1611.01144). *arXiv:1611.01144*.
- 2017\. A. V. D. Oord, O. Vinyals, et al. [Neural discrete representation learning](https://arxiv.org/abs/1711.00937). *NeurIPS*.
- 2021\. Rishi Bommasani et al. [On the Opportunities and Risks of Foundation Models](https://arxiv.org/abs/2108.07258). *arXiv preprint arXiv:2108.07258*.
- 2021\. Sabrina J. Mielke et al. [Between Words and Characters: A Brief History of Open-Vocabulary Modeling and Tokenization in NLP](https://arxiv.org/abs/2112.10508). *arXiv preprint arXiv:2112.10508*.
- 2025\. Juan Luis Gastaldi, John Terilla, Luca Malagutti, Brian DuSell, Tim Vieira, and Ryan Cotterell. [The Foundations of Tokenization: Statistical and Computational Concerns](https://arxiv.org/abs/2407.11606). *International Conference on Learning Representations*.
- 2025\. Marco Cognetta and Naoaki Okazaki. [Tokenization as Finite-State Transduction](https://aclanthology.org/2025.cl-4.2/). *Computational Linguistics*.
- 2026\. Mohammad Mahdi Azizi, Bagher BabaAli, Fatemeh Ziaeetabar. [Dynamic Tokenization in the Transformer Era: A Review and Taxonomy](https://doi.org/10.1016/j.patcog.2026.114439). *Pattern Recognition*.

## 1.1 Text and Code

- 2002\. Mathias Creutz and Krista Lagus. [Unsupervised Discovery of Morphemes](https://aclanthology.org/W02-0603/). *Workshop on Morphological and Phonological Learning*.
- 2012\. Mike Schuster and Kaisuke Nakajima. [Japanese and Korean Voice Search](https://doi.org/10.1109/ICASSP.2012.6289079). *IEEE ICASSP*.
- 2016\. Rico Sennrich, Barry Haddow, Alexandra Birch. [Neural Machine Translation of Rare Words with Subword Units](https://aclanthology.org/P16-1162/). *Proceedings of ACL*.
- 2017\. Ashish Vaswani et al. [Attention Is All You Need](https://papers.neurips.cc/paper/7181-attention-is-all-you-need.pdf). *Advances in Neural Information Processing Systems*.
- 2018\. Taku Kudo, John Richardson. [SentencePiece: A Simple and Language Independent Subword Tokenizer and Detokenizer for Neural Text Processing](https://arxiv.org/abs/1808.06226). *Proceedings of EMNLP: System Demonstrations*.
- 2018\. Taku Kudo. [Subword Regularization: Improving Neural Network Translation Models with Multiple Subword Candidates](https://aclanthology.org/P18-1007/). *ACL*.
- 2020\. Ivan Provilkov, Dmitrii Emelianenko, and Elena Voita. [BPE-Dropout: Simple and Effective Subword Regularization](https://aclanthology.org/2020.acl-main.170/). *ACL*.
- 2020\. Kaj Bostrom and Greg Durrett. [Byte Pair Encoding Is Suboptimal for Language Model Pretraining](https://aclanthology.org/2020.findings-emnlp.414/). *Findings of EMNLP*.
- 2020\. Tom B. Brown et al. [Language Models Are Few-Shot Learners](https://proceedings.neurips.cc/paper/2020/hash/1457c0d6bfcb4967418bfb8ac142f64a-Abstract.html). *Advances in Neural Information Processing Systems*.
- 2020\. Jonathan Herzig et al. [TAPAS: Weakly Supervised Table Parsing via Pre-training](https://arxiv.org/abs/2004.02349). *ACL*.
- 2021\. Phillip Rust, Jonas Pfeiffer, Ivan Vulić, Sebastian Ruder, and Iryna Gurevych. [How Good Is Your Tokenizer? On the Monolingual Performance of Multilingual Language Models](https://aclanthology.org/2021.acl-long.243/). *ACL*.
- 2022\. Jonathan H. Clark et al. [CANINE: Pre-training an Efficient Tokenization-Free Encoder for Language Representation](https://aclanthology.org/2022.tacl-1.5/). *Transactions of the Association for Computational Linguistics*.
- 2022\. Linting Xue et al. [ByT5: Towards a Token-Free Future with Pre-trained Byte-to-Byte Models](https://aclanthology.org/2022.tacl-1.17/). *Transactions of the Association for Computational Linguistics*.
- 2022\. Yi Tay et al. [Charformer: Fast Character Transformers via Gradient-Based Subword Tokenization](https://openreview.net/forum?id=JtBRnrlOEFN). *International Conference on Learning Representations*.
- 2023\. Aleksandar Petrov, Emanuele La Malfa, Philip Torr, Adel Bibi. [Language Model Tokenizers Introduce Unfairness Between Languages](https://proceedings.neurips.cc/paper_files/paper/2023/hash/74bb24dca8334adce292883b4b651eda-Abstract-Conference.html). *Advances in Neural Information Processing Systems*.
- 2023\. Lili Yu et al. [MEGABYTE: Predicting Million-Byte Sequences with Multiscale Transformers](https://proceedings.neurips.cc/paper_files/paper/2023/hash/f8f78f8043f35890181a824e53a57134-Abstract-Conference.html). *Advances in Neural Information Processing Systems*.
- 2023\. Alec Radford et al. [Robust Speech Recognition via Large-Scale Weak Supervision](https://arxiv.org/abs/2212.04356). *International Conference on Machine Learning*.
- 2023\. Jade Copet et al. [Simple and Controllable Music Generation](https://arxiv.org/abs/2306.05284). *Advances in Neural Information Processing Systems*.
- 2024\. Artidoro Pagnoni et al. [Byte Latent Transformer: Patches Scale Better Than Tokens](https://arxiv.org/abs/2412.09871). *arXiv preprint arXiv:2412.09871*.
- 2024\. Anton Lozhkov et al. [StarCoder 2 and The Stack v2: The Next Generation](https://arxiv.org/abs/2402.19173). *arXiv preprint arXiv:2402.19173*.
- 2024\. Haotian Liu et al. [Improved Baselines with Visual Instruction Tuning](https://arxiv.org/abs/2310.03744). *IEEE/CVF Conference on Computer Vision and Pattern Recognition*.
- 2024\. Patrick Esser et al. [Scaling Rectified Flow Transformers for High-Resolution Image Synthesis](https://arxiv.org/abs/2403.03206). *International Conference on Machine Learning*.
- 2024\. Craig W. Schmidt et al. [Tokenization Is More Than Compression](https://aclanthology.org/2024.emnlp-main.40/). *Proceedings of EMNLP*.
- 2024\. Darius Fehér, Ivan Vulić, and Benjamin Minixhofer. [Retrofitting Large Language Models with Dynamic Tokenization](https://arxiv.org/abs/2411.18553). *arXiv*.
- 2024\. DeepSeek-AI. [DeepSeek LLM: Scaling Open-Source Language Models with Longtermism](https://arxiv.org/abs/2401.02954). *arXiv preprint arXiv:2401.02954*.
- 2024\. DeepSeek-AI. [DeepSeek-V3 Technical Report](https://arxiv.org/abs/2412.19437). *arXiv preprint arXiv:2412.19437*.
- 2024\. Gautier Dagan, Gabriel Synnaeve, and Baptiste Roziere. [Getting the Most out of Your Tokenizer for Pre-Training and Domain Adaptation](https://proceedings.mlr.press/v235/dagan24a.html). *International Conference on Machine Learning*.
- 2024\. Junxiong Wang et al. [MambaByte: Token-Free Selective State Space Model](https://openreview.net/forum?id=X1xNsuKssb). *Conference on Language Modeling*.
- 2024\. Llama Team. [The Llama 3 Herd of Models](https://arxiv.org/abs/2407.21783). *arXiv preprint arXiv:2407.21783*.
- 2024\. Mehdi Ali et al. [Tokenizer Choice for LLM Training: Negligible or Crucial?](https://aclanthology.org/2024.findings-naacl.247/). *Findings of NAACL*.
- 2024\. Mistral AI Team. [Mistral NeMo](https://mistral.ai/news/mistral-nemo/). *Mistral AI Technical Release*.
- 2024\. Omer Goldman et al. [Unpacking Tokenization: Evaluating Text Compression and Its Correlation with Model Performance](https://aclanthology.org/2024.findings-acl.134/). *Findings of ACL*.
- 2024\. Omri Uzan, Craig W. Schmidt, Chris Tanner, and Yuval Pinter. [Greed Is All You Need: An Evaluation of Tokenizer Inference Methods](https://aclanthology.org/2024.acl-short.73/). *ACL*.
- 2024\. Qwen Team. [Qwen2 Technical Report](https://arxiv.org/abs/2407.10671). *arXiv preprint arXiv:2407.10671*.
- 2024\. Qwen Team. [Qwen2.5 Technical Report](https://arxiv.org/abs/2412.15115). *arXiv preprint arXiv:2412.15115*.
- 2024\. Xingwu Sun et al. [Hunyuan-Large: An Open-Source MoE Model with 52 Billion Activated Parameters by Tencent](https://arxiv.org/abs/2411.02265). *arXiv preprint arXiv:2411.02265*.
- 2024\. Yekun Chai, Yewei Fang, Qiwei Peng, and Xuhong Li. [Tokenization Falling Short: On Subword Robustness in Large Language Models](https://aclanthology.org/2024.findings-emnlp.86/). *Findings of EMNLP*.
- 2025\. Catherine Arnett, Tyler Chang, Stella Biderman, and Benjamin Bergen. [Explaining and Mitigating Crosslingual Tokenizer Inequities](https://proceedings.neurips.cc/paper_files/paper/2025/hash/5b91cefbfa52340af2f16f249572dc76-Abstract-Conference.html). *NeurIPS*.
- 2024\. Zhuoyi Yang et al. [CogVideoX: Text-to-Video Diffusion Models with An Expert Transformer](https://arxiv.org/abs/2408.06072). *arXiv preprint arXiv:2408.06072*.
- 2025\. Qwen Team. [Qwen2.5-VL Technical Report](https://arxiv.org/abs/2502.13923). *arXiv preprint arXiv:2502.13923*.
- 2025\. Hao Chen et al. [Masked Autoencoders Are Effective Tokenizers for Diffusion Models](https://proceedings.mlr.press/v267/chen25v.html). *International Conference on Machine Learning*.
- 2025\. Hongzhi Huang et al. [Over-Tokenized Transformer: Vocabulary Is Generally Worth Scaling](https://proceedings.mlr.press/v267/huang25bb.html). *International Conference on Machine Learning*.
- 2025\. Jia Peng Lim, Shawn Tan, Davin Choo, and Hady W. Lauw. [A Partition Cover Approach to Tokenization](https://proceedings.neurips.cc/paper_files/paper/2025/hash/605e59e78284907aa4fce5280838def3-Abstract-Conference.html). *NeurIPS*.
- 2025\. Kimi Team. [Kimi K2: Open Agentic Intelligence](https://arxiv.org/abs/2507.20534). *arXiv preprint arXiv:2507.20534*.
- 2025\. Preston Firestone, Shubham Ugare, Gagandeep Singh, and Sasa Misailovic. [UTF-8 Plumbing: Byte-Level Tokenizers Unavoidably Enable LLMs to Generate Ill-Formed UTF-8](https://openreview.net/forum?id=8ExXncFpf6). *Conference on Language Modeling*.
- 2025\. Saibo Geng, Nathan Ranchin, Yunzhen Yao, Maxime Peyrard, Chris Wendler, Michael Gastpar, and Robert West. [zip2zip: Inference-Time Adaptive Tokenization via Online Compression](https://proceedings.neurips.cc/paper_files/paper/2025/hash/def682d57535b9e778508b4b1a911034-Abstract-Conference.html). *NeurIPS*.
- 2025\. Tim Vieira et al. [From Language Models over Tokens to Language Models over Characters](https://proceedings.mlr.press/v267/vieira25a.html). *International Conference on Machine Learning*.

## 1.2 Images and Video

- 2019\. A. Razavi, A. V. D. Oord, et al. [Generating diverse high-fidelity images with vq-vae-2](https://arxiv.org/abs/1906.00446). *NeurIPS*.
- 2021\. Aditya Ramesh et al. [Zero-Shot Text-to-Image Generation](https://proceedings.mlr.press/v139/ramesh21a.html). *ICML*.
- 2021\. Alexey Dosovitskiy et al. [An Image Is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://openreview.net/forum?id=YicbFdNTTy). *International Conference on Learning Representations*.
- 2021\. Anurag Arnab et al. [ViViT: A Video Vision Transformer](https://arxiv.org/abs/2103.15691). *International Conference on Computer Vision*.
- 2021\. H. Bao, L. Dong, et al. [Beit: Bert pre-training of image transformers](https://openreview.net/forum?id=p-BhZSz59o4). *arXiv*.
- 2021\. Michael S. Ryoo, AJ Piergiovanni, Anurag Arnab, Mostafa Dehghani, and Anelia Angelova. [TokenLearner: Adaptive Space-Time Tokenization for Videos](https://proceedings.neurips.cc/paper/2021/hash/6a30e32e56fce5cf381895dfe6ca7b6f-Abstract.html). *NeurIPS*.
- 2021\. P. Esser, R. Rombach, et al. [Taming transformers for high-resolution image synthesis](https://openaccess.thecvf.com/content/CVPR2021/html/Esser_Taming_Transformers_for_High-Resolution_Image_Synthesis_CVPR_2021_paper.html). *CVPR*.
- 2021\. W. Yan, Y. Zhang, et al. [Videogpt: Video generation using vq-vae and transformers](https://arxiv.org/abs/2104.10157). *arXiv*.
- 2021\. Yongming Rao et al. [DynamicViT: Efficient Vision Transformers with Dynamic Token Sparsification](https://proceedings.neurips.cc/paper_files/paper/2021/hash/747d3443e319a22747fbb873e8b2f9f2-Abstract.html). *NeurIPS*.
- 2022\. D. Lee, C. Kim, et al. [Autoregressive image generation using residual quantization](https://openaccess.thecvf.com/content/CVPR2022/html/Lee_Autoregressive_Image_Generation_Using_Residual_Quantization_CVPR_2022_paper.html). *CVPR*.
- 2022\. H. Chang, H. Zhang, et al. [Maskgit: Masked generative image transformer](https://openaccess.thecvf.com/content/CVPR2022/html/Chang_MaskGIT_Masked_Generative_Image_Transformer_CVPR_2022_paper.html). *CVPR*.
- 2022\. Richard J. Chen, Chengkuan Chen, Yicong Li, Tiffany Y. Chen, Andrew D. Trister, Rahul G. Krishnan, and Faisal Mahmood. [Scaling Vision Transformers to Gigapixel Images via Hierarchical Self-Supervised Learning](https://openaccess.thecvf.com/content/CVPR2022/html/Chen_Scaling_Vision_Transformers_to_Gigapixel_Images_via_Hierarchical_Self-Supervised_Learning_CVPR_2022_paper.html). *CVPR*.
- 2022\. Youwei Liang et al. [Not All Patches Are What You Need: Expediting Vision Transformers via Token Reorganizations](https://openreview.net/forum?id=BjyvwnXXVn_). *ICLR*.
- 2022\. Zhan Tong, Yibing Song, Jue Wang, Limin Wang. [VideoMAE: Masked Autoencoders Are Data-Efficient Learners for Self-Supervised Video Pre-Training](https://arxiv.org/abs/2203.12602). *Advances in Neural Information Processing Systems*.
- 2023\. Daniel Bolya, Cheng-Yang Fu, Xiaoliang Dai, Peizhao Zhang, Christoph Feichtenhofer, Judy Hoffman. [Token Merging: Your ViT but Faster](https://openreview.net/forum?id=JroZRaRw7Eu). *International Conference on Learning Representations*.
- 2023\. L. Yu, Y. Cheng, et al. [Magvit: Masked generative video transformer](https://openaccess.thecvf.com/content/CVPR2023/html/Yu_MAGVIT_Masked_Generative_Video_Transformer_CVPR_2023_paper.html). *CVPR*.
- 2023\. Mahmoud Assran et al. [Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture](https://arxiv.org/abs/2301.08243). *Conference on Computer Vision and Pattern Recognition*.
- 2023\. Alexander Kirillov et al. [Segment Anything](https://arxiv.org/abs/2304.02643). *IEEE/CVF International Conference on Computer Vision*.
- 2024\. Adrien Bardes et al. [Revisiting Feature Prediction for Learning Visual Representations from Video](https://arxiv.org/abs/2404.08471). *European Conference on Computer Vision*.
- 2024\. Haotian Liu et al. [Improved Baselines with Visual Instruction Tuning](https://arxiv.org/abs/2310.03744). *IEEE/CVF Conference on Computer Vision and Pattern Recognition*.
- 2024\. Patrick Esser et al. [Scaling Rectified Flow Transformers for High-Resolution Image Synthesis](https://arxiv.org/abs/2403.03206). *International Conference on Machine Learning*.
- 2024\. Dan Kondratyuk et al. [VideoPoet: A Large Language Model for Zero-Shot Video Generation](https://arxiv.org/abs/2312.14125). *International Conference on Machine Learning*.
- 2024\. F. Mentzer, D. Minnen, et al. [Finite Scalar Quantization: VQ-VAE Made Simple](https://openreview.net/forum?id=8ishA3LxN8). *ICLR*.
- 2024\. Jiahui Wang et al. [OmniTokenizer: A Joint Image-Video Tokenizer for Visual Generation](https://proceedings.neurips.cc/paper_files/paper/2024/hash/31994923f58ae5b2d661b300bd439107-Abstract-Conference.html). *NeurIPS*.
- 2024\. K. Tian, Y. Jiang, et al. [Visual autoregressive modeling: Scalable image generation via next-scale prediction](https://proceedings.neurips.cc/paper_files/paper/2024/hash/9a24e284b187f662681440ba15c416fb-Abstract-Conference.html). *NeurIPS*.
- 2024\. Lijun Yu et al. [Language Model Beats Diffusion: Tokenizer Is Key to Visual Generation](https://openreview.net/forum?id=gzqrANCF4g). *ICLR*.
- 2024\. Meta Movie Gen Team. [Movie Gen: A Cast of Media Foundation Models](https://arxiv.org/abs/2410.13720). *arXiv preprint arXiv:2410.13720*.
- 2024\. Q. Yu, M. Weber, et al. [An image is worth 32 tokens for reconstruction and generation](https://proceedings.neurips.cc/paper_files/paper/2024/hash/e91bf7dfba0477554994c6d64833e9d8-Abstract-Conference.html). *NeurIPS*.
- 2024\. Ritwik Gupta, Shufan Li, Tyler Zhu, Jitendra Malik, Trevor Darrell, and Karttikeya Mangalam. [xT: Nested Tokenization for Larger Context in Large Images](https://proceedings.mlr.press/v235/gupta24b.html). *International Conference on Machine Learning*.
- 2024\. Weijie Kong et al. [HunyuanVideo: A Systematic Framework for Large Video Generative Models](https://arxiv.org/abs/2412.03603). *arXiv preprint arXiv:2412.03603*.
- 2024\. Yang Jin, Zhicheng Sun, Kun Xu, Kun Xu, Liwei Chen, Hao Jiang, Quzhe Huang, Chengru Song, Yuliang Liu, Di Zhang, Yang Song, Kun Gai, and Yadong Mu. [Video-LaVIT: Unified Video-Language Pre-Training with Decoupled Visual-Motional Tokenization](https://proceedings.mlr.press/v235/jin24f.html). *International Conference on Machine Learning*.
- 2024\. Zhuoyi Yang et al. [CogVideoX: Text-to-Video Diffusion Models with An Expert Transformer](https://arxiv.org/abs/2408.06072). *arXiv preprint arXiv:2408.06072*.
- 2025\. Adrian Bulat, Yassine Ouali, and Georgios Tzimiropoulos. [Compress & Cache: Vision Token Compression for Efficient Generation and Retrieval](https://proceedings.neurips.cc/paper_files/paper/2025/hash/2e01083b381b4865919b4915ef32e3d2-Abstract-Conference.html). *NeurIPS*.
- 2025\. Qwen Team. [Qwen2.5-VL Technical Report](https://arxiv.org/abs/2502.13923). *arXiv preprint arXiv:2502.13923*.
- 2025\. Anlin Zheng, Xin Wen, Xuanyang Zhang, Chuofan Ma, Tiancai Wang, Gang Yu, Xiangyu Zhang, and Xiaojuan Qi. [Vision Foundation Models as Effective Visual Tokenizers for Autoregressive Generation](https://proceedings.neurips.cc/paper_files/paper/2025/hash/5a829e299ebc1c1615ddb09e98fb6ce8-Abstract-Conference.html). *NeurIPS*.
- 2025\. Chuofan Ma et al. [UniTok: A Unified Tokenizer for Visual Generation and Understanding](https://proceedings.neurips.cc/paper_files/paper/2025/hash/bbe04d329d531e8814f1199098bd8fb6-Abstract-Conference.html). *NeurIPS*.
- 2025\. Duy-Kien Nguyen, Mahmoud Assran, Unnat Jain, Martin R. Oswald, Cees G. M. Snoek, and Xinlei Chen. [An Image Is Worth More Than 16x16 Patches: Exploring Transformers on Individual Pixels](https://arxiv.org/abs/2406.09415). *International Conference on Learning Representations*.
- 2025\. Feng Wang, Yaodong Yu, Wei Shao, Yuyin Zhou, Alan Yuille, and Cihang Xie. [Scaling Laws in Patchification: An Image Is Worth 50,176 Tokens And More](https://proceedings.mlr.press/v267/wang25ed.html). *International Conference on Machine Learning*.
- 2025\. Huawei Lin, Tong Geng, Zhaozhuo Xu, and Weijie Zhao. [VTBench: Evaluating Visual Tokenizers for Autoregressive Image Generation](https://arxiv.org/abs/2505.13439). *arXiv*.
- 2025\. Jiaming Han, Hao Chen, Yang Zhao, Hanyu Wang, Qi Zhao, Ziyan Yang, Hao He, Xiangyu Yue, and Lu Jiang. [Vision as a Dialect: Unifying Visual Understanding and Generation via Text-Aligned Representations](https://proceedings.neurips.cc/paper_files/paper/2025/hash/e87b1e06be8c3594c810e8991e77ea40-Abstract-Conference.html). *NeurIPS*.
- 2025\. Junfeng Wu et al. [TokBench: Evaluating Your Visual Tokenizer before Visual Generation](https://arxiv.org/abs/2505.18142). *arXiv*.
- 2025\. Junhong Shen et al. [CAT: Content-Adaptive Image Tokenization](https://proceedings.neurips.cc/paper_files/paper/2025/hash/014898b821e3ce966ae1db68cb8d9966-Abstract-Conference.html). *NeurIPS*.
- 2025\. Kyle Sargent, Kyle Hsu, Justin Johnson, Li Fei-Fei, and Jiajun Wu. [Flow to the Mode: Mode-Seeking Diffusion Autoencoders for State-of-the-Art Image Tokenization](https://openaccess.thecvf.com/content/ICCV2025/html/Sargent_Flow_to_the_Mode_Mode-Seeking_Diffusion_Autoencoders_for_State-of-the-Art_Image_ICCV_2025_paper.html). *ICCV*.
- 2025\. Lijun Qu et al. [TokenFlow: Unified Image Tokenizer for Multimodal Understanding and Generation](https://openaccess.thecvf.com/content/CVPR2025/html/Qu_TokenFlow_Unified_Image_Tokenizer_for_Multimodal_Understanding_and_Generation_CVPR_2025_paper.html). *CVPR*.
- 2025\. Lingfeng Wang et al. [ALTo: Adaptive-Length Tokenizer for Autoregressive Mask Generation](https://proceedings.neurips.cc/paper_files/paper/2025/hash/17a9ab4190289f0e1504bbb98d1d111a-Abstract-Conference.html). *NeurIPS*.
- 2025\. Long Zhao et al. [Epsilon-VAE: Denoising as Visual Decoding](https://proceedings.mlr.press/v267/zhao25w.html). *International Conference on Machine Learning*.
- 2025\. Minghao Yang, Zechen Bai, Jing Lin, Haoqian Wang, and Alex Jinpeng Wang. [VaporTok: RL-Driven Adaptive Video Tokenizer with Prior and Task Awareness](https://proceedings.neurips.cc/paper_files/paper/2025/hash/43e41fa7544d2ee435c72305702de61f-Abstract-Conference.html). *NeurIPS*.
- 2025\. Philippe Hansen-Estruch et al. [Learnings from Scaling Visual Tokenizers for Reconstruction and Generation](https://arxiv.org/abs/2501.09755). *arXiv*.
- 2025\. Siyuan Li et al. [MergeVQ: A Unified Framework for Visual Generation and Representation with Disentangled Token Merging and Quantization](https://openaccess.thecvf.com/content/CVPR2025/html/Li_MergeVQ_A_Unified_Framework_for_Visual_Generation_and_Representation_with_CVPR_2025_paper.html). *CVPR*.
- 2025\. StepFun-AI Team. [Step-Video-T2V Technical Report: The Practice, Challenges, and Future of Video Foundation Model](https://arxiv.org/abs/2502.10248). *arXiv preprint arXiv:2502.10248*.
- 2025\. Vivek Ramanujan, Kushal Tirumala, Armen Aghajanyan, Luke Zettlemoyer, and Ali Farhadi. [When Worse Is Better: Navigating the Compression Generation Trade-off in Visual Tokenization](https://proceedings.neurips.cc/paper_files/paper/2025/hash/b6425ecad28e4960cb4a622beb338ffe-Abstract-Conference.html). *NeurIPS*.
- 2025\. Wan Team. [Wan: Open and Advanced Large-Scale Video Generative Models](https://arxiv.org/abs/2503.20314). *arXiv preprint arXiv:2503.20314*.
- 2025\. Wanpeng Zhang, Zilong Xie, Yicheng Feng, Yijiang Li, Xingrun Xing, Sipeng Zheng, and Zongqing Lu. [From Pixels to Tokens: Byte-Pair Encoding on Quantized Visual Modalities](https://proceedings.iclr.cc/paper_files/paper/2025/hash/68933e3533add841e115a5605c76eeba-Abstract-Conference.html). *International Conference on Learning Representations*.
- 2025\. Wenxuan Wang et al. [End-to-End Vision Tokenizer Tuning](https://proceedings.neurips.cc/paper_files/paper/2025/hash/445019c840424130e04c95c664408e8d-Abstract-Conference.html). *NeurIPS*.
- 2025\. Yifan Zha et al. [Language-Guided Image Tokenization for Generation](https://openaccess.thecvf.com/content/CVPR2025/html/Zha_Language-Guided_Image_Tokenization_for_Generation_CVPR_2025_paper.html). *CVPR*.
- 2025\. Yue Zhao, Yuanjun Xiong, and Philipp Krähenbühl. [Image and Video Tokenization with Binary Spherical Quantization](https://openreview.net/forum?id=yGnsH3gQ6U). *ICLR*.
- 2025\. Zhengqiang Zhang, Rongyuan Wu, Lingchen Sun, and Lei Zhang. [GPSToken: Gaussian Parameterized Spatially-Adaptive Tokenization for Image Representation and Generation](https://proceedings.neurips.cc/paper_files/paper/2025/hash/10831838f1cdd8fcba90188e88e7a121-Abstract-Conference.html). *NeurIPS*.

## 1.3 Audio and Speech

- 2019\. A. Baevski, S. Schneider, et al. [vq-wav2vec: Self-supervised learning of discrete speech representations](https://openreview.net/forum?id=rylwJxrYDS). *arXiv*.
- 2020\. A. Baevski, Y. Zhou, et al. [wav2vec 2.0: A Framework for Self-Supervised Learning of Speech Representations](https://proceedings.neurips.cc/paper/2020/hash/92d1e1eb1cd6f9fba3227870bb6d7f07-Abstract.html). *NeurIPS*.
- 2021\. Kushal Lakhotia et al. [On Generative Spoken Language Modeling from Raw Audio](https://aclanthology.org/2021.tacl-1.79/). *Transactions of the Association for Computational Linguistics*.
- 2021\. N. Zeghidour, A. Luebs, et al. [Soundstream: An end-to-end neural audio codec](https://arxiv.org/abs/2107.03312). *TASLP*.
- 2021\. Wei-Ning Hsu et al. [HuBERT: Self-Supervised Speech Representation Learning by Masked Prediction of Hidden Units](https://doi.org/10.1109/TASLP.2021.3122291). *IEEE/ACM Transactions on Audio, Speech, and Language Processing*.
- 2022\. Zalán Borsos et al. [AudioLM: A Language Modeling Approach to Audio Generation](https://arxiv.org/abs/2209.03143). *arXiv*.
- 2022\. Alec Radford et al. [Robust Speech Recognition via Large-Scale Weak Supervision](https://arxiv.org/abs/2212.04356). *arXiv preprint arXiv:2212.04356*.
- 2023\. A. Defossez, J. Copet, et al. [High Fidelity Neural Audio Compression](https://openreview.net/forum?id=ivCd8z8zR2). *TMLR*.
- 2023\. Jade Copet et al. [Simple and Controllable Music Generation](https://arxiv.org/abs/2306.05284). *Advances in Neural Information Processing Systems*.
- 2023\. Andrea Agostinelli et al. [MusicLM: Generating Music From Text](https://arxiv.org/abs/2301.11325). *arXiv*.
- 2023\. C. Wang, S. Chen, et al. [Neural codec language models are zero-shot text to speech synthesizers](https://arxiv.org/abs/2301.02111). *arXiv*.
- 2023\. Rithesh Kumar, Prem Seetharaman, Alejandro Luebs, Ishaan Kumar, and Kundan Kumar. [High-Fidelity Audio Compression with Improved RVQGAN](https://proceedings.neurips.cc/paper_files/paper/2023/hash/58d0e78cf042af5876e12661087bea12-Abstract-Conference.html). *NeurIPS*.
- 2024\. Hubert Siuzdak, Florian Grötschla, and Luca A. Lanzendörfer. [SNAC: Multi-Scale Neural Audio Codec](https://arxiv.org/abs/2410.14411). *arXiv*.
- 2024\. Pooneh Mousavi et al. [DASB: Discrete Audio and Speech Benchmark](https://arxiv.org/abs/2406.14294). *arXiv*.
- 2024\. Z. Xin, Z. Dong, et al. [Speechtokenizer: Unified speech tokenizer for speech language models](https://openreview.net/forum?id=AF9Q8Vy3lj). *ICLR*.
- 2024\. Zhichao Huang, Chutong Meng, and Tom Ko. [RepCodec: A Speech Representation Codec for Speech Tokenization](https://aclanthology.org/2024.acl-long.314/). *ACL*.
- 2025\. Dongchao Yang et al. [ALMTokenizer: A Low-bitrate and Semantic-rich Audio Codec Tokenizer for Audio Language Modeling](https://proceedings.mlr.press/v267/yang25q.html). *International Conference on Machine Learning*.
- 2025\. Pooneh Mousavi et al. [Discrete Audio Tokens: More Than a Survey!](https://arxiv.org/abs/2506.10274). *arXiv*.
- 2025\. Wenrui Liu et al. [Analyzing and Mitigating Inconsistency in Discrete Speech Tokens for Neural Codec Language Models](https://aclanthology.org/2025.acl-long.1498/). *ACL*.
- 2025\. Yuancheng Wang, Dekun Chen, Xueyao Zhang, Junan Zhang, Jiaqi Li, and Zhizheng Wu. [TaDiCodec: Text-Aware Diffusion Speech Tokenizer for Speech Language Modeling](https://proceedings.neurips.cc/paper_files/paper/2025/hash/d8a12fde9e72444e1b356e8c37e53753-Abstract-Conference.html). *NeurIPS*.

## 1.4 Point Clouds and Three-Dimensional Structure

- 2022\. Xumin Yu, Lulu Tang, Yongming Rao, Tiejun Huang, Jie Zhou, and Jiwen Lu. [Point-BERT: Pre-Training 3D Point Cloud Transformers With Masked Point Modeling](https://openaccess.thecvf.com/content/CVPR2022/html/Yu_Point-BERT_Pre-Training_3D_Point_Cloud_Transformers_With_Masked_Point_Modeling_CVPR_2022_paper.html). *IEEE/CVF Conference on Computer Vision and Pattern Recognition*.
- 2025\. Xiaoyang Wu et al. [Sonata: Self-Supervised Learning of Reliable Point Representations](https://arxiv.org/abs/2503.16429). *IEEE/CVF Conference on Computer Vision and Pattern Recognition*.
- 2025\. Jian Liu et al. [FreeMesh: Boosting Mesh Generation with Coordinates Merging](https://proceedings.mlr.press/v267/liu25bz.html). *International Conference on Machine Learning*.

## 1.5 Graphs and Tables

- 2011\. Nino Shervashidze et al. [Weisfeiler-Lehman Graph Kernels](https://www.jmlr.org/papers/v12/shervashidze11a.html). *Journal of Machine Learning Research*.
- 2017\. Annamalai Narayanan et al. [graph2vec: Learning Distributed Representations of Graphs](https://arxiv.org/abs/1707.05005). *Mining and Learning with Graphs Workshop*.
- 2020\. Xin Huang et al. [TabTransformer: Tabular Data Modeling Using Contextual Embeddings](https://arxiv.org/abs/2012.06678). *arXiv*.
- 2020\. Jonathan Herzig et al. [TAPAS: Weakly Supervised Table Parsing via Pre-training](https://arxiv.org/abs/2004.02349). *ACL*.
- 2021\. M. Galkin, E. Denis, et al. [Nodepiece: Compositional and parameter-efficient representations of large knowledge graphs](https://openreview.net/forum?id=xMJWUKJnFSw). *arXiv*.
- 2021\. Yury Gorishniy, Ivan Rubachev, Valentin Khrulkov, Artem Babenko. [Revisiting Deep Learning Models for Tabular Data](https://proceedings.neurips.cc/paper/2021/hash/9d86d83f925f2149e9edb0ac3b49229c-Abstract.html). *Advances in Neural Information Processing Systems*.
- 2022\. Jinheon Baek et al. [Accurate Learning of Graph Representations with Graph Multiset Pooling](https://openreview.net/forum?id=JHcqXGaqiGn). *ICLR*.
- 2022\. Jinwoo Kim et al. [Pure Transformers Are Powerful Graph Learners](https://proceedings.neurips.cc/paper_files/paper/2022/hash/5d84236751fe6d25dc06db055a3180b0-Abstract-Conference.html). *NeurIPS*.
- 2023\. Shashank Rajput, Nikhil Mehta, Anima Singh, Raghunandan Hulikal Keshavan, Trung Vu, Lukasz Heldt, Lichan Hong, Yi Tay, Vinh Tran, Jonah Samost, Maciej Kula, Ed Chi, and Maheswaran Sathiamoorthy. [Recommender Systems with Generative Retrieval](https://proceedings.neurips.cc/paper_files/paper/2023/hash/20dcab0f14046a5c6b02b61da9f13229-Abstract-Conference.html). *NeurIPS*.
- 2024\. Haitao Mao et al. [Position: Graph Foundation Models Are Already Here](https://arxiv.org/abs/2402.02216). *International Conference on Machine Learning*.
- 2024\. Wenjie Wang, Honghui Bao, Xinyu Lin, Jizhi Zhang, Yongqi Li, Fuli Feng, See-Kiong Ng, and Tat-Seng Chua. [Learnable Item Tokenization for Generative Recommendation](https://doi.org/10.1145/3627673.3679569). *ACM International Conference on Information and Knowledge Management*.
- 2024\. Ye Wang, Jiahao Xun, Minjie Hong, Jieming Zhu, Tao Jin, Wang Lin, Haoyuan Li, Linjun Li, Yan Xia, Zhou Zhao, and Zhenhua Dong. [EAGER: Two-Stream Generative Recommender with Behavior-Semantic Collaboration](https://doi.org/10.1145/3637528.3671775). *ACM SIGKDD Conference on Knowledge Discovery and Data Mining*.
- 2024\. Yinhan Chen et al. [Improving Graph-Language Alignment with Hierarchical Graph Tokenization](https://openreview.net/forum?id=Vy1VgUGnuJ). *ICML Workshop on Foundation Models in the Wild*.
- 2024\. Zehong Wang, Zheyuan Zhang, Nitesh V. Chawla, Chuxu Zhang, and Yanfang Ye. [GFT: Graph Foundation Model with Transferable Tree Vocabulary](https://proceedings.neurips.cc/paper_files/paper/2024/hash/c23ccf9eedf87e4380e92b75b24955bb-Abstract-Conference.html). *NeurIPS*.
- 2025\. Haonan Yuan, Qingyun Sun, Junhua Shi, Xingcheng Fu, Bryan Hooi, Jianxin Li, and Philip S. Yu. [GRAVER: Generative Graph Vocabularies for Robust Graph Foundation Models Fine-tuning](https://proceedings.neurips.cc/paper_files/paper/2025/file/185969291540b3cd86e70c51e8af5d08-Paper-Conference.pdf). *NeurIPS*.
- 2025\. L. Wang, K. Hassani, et al. [Learning Graph Quantized Tokenizers](https://openreview.net/forum?id=oYSsbY3G4o). *ICLR*.
- 2025\. Noah Hollmann, Samuel Muller, Lennart Purucker, Arjun Krishnakumar, Frank Hutter. [Accurate Predictions on Small Data with a Tabular Foundation Model](https://doi.org/10.1038/s41586-024-08328-6). *Nature*.
- 2025\. Yupeng Hou, Jiacheng Li, Ashley Shin, Jinsung Jeon, Abhishek Santhanam, Wei Shao, Kaveh Hassani, Ning Yao, and Julian McAuley. [Generating Long Semantic IDs in Parallel for Recommendation](https://doi.org/10.1145/3711896.3736979). *ACM SIGKDD Conference on Knowledge Discovery and Data Mining*.
- 2025\. Zehong Wang, Zheyuan Zhang, Tianyi Ma, Chuxu Zhang, and Yanfang Ye. [Generative Graph Pattern Machine](https://proceedings.neurips.cc/paper_files/paper/2025/file/2b22bacd7ad8677f4837b28a11fe496f-Paper-Conference.pdf). *NeurIPS*.
- 2026\. Zeyuan Guo, Enmao Diao, Cheng Yang, and Chuan Shi. [Graph Tokenization for Bridging Graphs and Transformers](https://proceedings.iclr.cc/paper_files/paper/2026/hash/2c0781f2ed2d8054d4f27a19bd8c380b-Abstract-Conference.html). *International Conference on Learning Representations*.

## 1.6 Time Series, Physical Fields, and Latent World States

- 2003\. Jessica Lin, Eamonn Keogh, Stefano Lonardi, and Bill Chiu. [A Symbolic Representation of Time Series, with Implications for Streaming Algorithms](https://doi.org/10.1145/882082.882086). *ACM SIGMOD Workshop on Research Issues in Data Mining and Knowledge Discovery*.
- 2020\. Danijar Hafner et al. [Mastering Atari with Discrete World Models](https://arxiv.org/abs/2010.02193). *ICLR 2021*.
- 2023\. Yuqi Nie, Nam H. Nguyen, Phanwadee Sinthong, and Jayant Kalagnanam. [A Time Series Is Worth 64 Words: Long-Term Forecasting with Transformers](https://openreview.net/forum?id=Jbdc0vTOcol). *ICLR*.
- 2024\. Abdul Fatir Ansari et al. [Chronos: Learning the Language of Time Series](https://arxiv.org/abs/2403.07815). *arXiv preprint arXiv:2403.07815*.
- 2024\. Abhimanyu Das et al. [A Decoder-Only Foundation Model for Time-Series Forecasting](https://arxiv.org/abs/2310.10688). *arXiv preprint arXiv:2310.10688*.
- 2024\. Vijay Ekambaram et al. [Tiny Time Mixers (TTMs): Fast Pre-trained Models for Enhanced Zero/Few-Shot Forecasting of Multivariate Time Series](https://arxiv.org/abs/2401.03955). *arXiv preprint arXiv:2401.03955*.
- 2024\. Mononito Goswami et al. [MOMENT: A Family of Open Time-Series Foundation Models](https://proceedings.mlr.press/v235/goswami24a.html). *ICML*.
- 2024\. OpenAI. [Video Generation Models as World Simulators](https://openai.com/index/video-generation-models-as-world-simulators/). *OpenAI Technical Report*.
- 2025\. Luca Masserano et al. [Enhancing Foundation Models for Time Series Forecasting via Wavelet-Based Tokenization](https://proceedings.mlr.press/v267/masserano25a.html). *ICML*.

## 1.7 Robot Actions and Embodied Trajectory

- 2024\. Jake Bruce et al. [Genie: Generative Interactive Environments](https://arxiv.org/abs/2402.15391). *arXiv*.
- 2024\. Jialong Wu, Shaofeng Yin, Ningya Feng, Xu He, Dong Li, Jianye Hao, and Mingsheng Long. [iVideoGPT: Interactive VideoGPTs Are Scalable World Models](https://proceedings.neurips.cc/paper_files/paper/2024/hash/7dbb5bfab324e3b86af9bd0df15498dd-Abstract-Conference.html). *NeurIPS*.
- 2024\. Ruijie Zheng, Ching-An Cheng, Hal Daumé III, Furong Huang, and Andrey Kolobov. [PRISE: LLM-Style Sequence Compression for Learning Temporal Action Abstractions in Control](https://proceedings.mlr.press/v235/zheng24b.html). *ICML*.
- 2025\. Karl Pertsch et al. [FAST: Efficient Action Tokenization for Vision-Language-Action Models](https://arxiv.org/abs/2501.09747). *arXiv*.
- 2025\. NVIDIA. [Cosmos World Foundation Model Platform for Physical AI](https://arxiv.org/abs/2501.03575). *arXiv preprint arXiv:2501.03575*.

## 1.8 Multimodal Token Systems

- 2021\. Andrew Jaegle et al. [Perceiver: General Perception with Iterative Attention](https://proceedings.mlr.press/v139/jaegle21a.html). *International Conference on Machine Learning*.
- 2022\. Jean-Baptiste Alayrac et al. [Flamingo: A Visual Language Model for Few-Shot Learning](https://arxiv.org/abs/2204.14198). *arXiv preprint arXiv:2204.14198*.
- 2023\. David Mizrahi, Roman Bachmann, Oğuzhan Fatih Kar, Teresa Yeo, Mingfei Gao, Afshin Dehghan, and Amir Zamir. [4M: Massively Multimodal Masked Modeling](https://proceedings.neurips.cc/paper_files/paper/2023/hash/b6446566965fa38e183650728ab70318-Abstract-Conference.html). *NeurIPS*.
- 2023\. Haotian Liu, Chunyuan Li, Qingyang Wu, and Yong Jae Lee. [Visual Instruction Tuning](https://arxiv.org/abs/2304.08485). *NeurIPS*.
- 2023\. Junnan Li, Dongxu Li, Silvio Savarese, and Steven Hoi. [BLIP-2: Bootstrapping Language-Image Pre-training with Frozen Image Encoders and Large Language Models](https://proceedings.mlr.press/v202/li23q.html). *ICML*.
- 2023\. Jade Copet et al. [Simple and Controllable Music Generation](https://arxiv.org/abs/2306.05284). *Advances in Neural Information Processing Systems*.
- 2023\. OpenAI. [GPT-4 Technical Report](https://arxiv.org/abs/2303.08774). *arXiv preprint arXiv:2303.08774*.
- 2024\. Amazon Artificial General Intelligence. [The Amazon Nova Family of Models: Technical Report and Model Card](https://www.amazon.science/publications/the-amazon-nova-family-of-models-technical-report-and-model-card). *Amazon Technical Reports*.
- 2024\. Anthropic. [The Claude 3 Model Family: Opus, Sonnet, Haiku](https://assets.anthropic.com/m/61e7d27f8c8f5919/original/Claude-3-Model-Card.pdf). *Anthropic Model Card*.
- 2024\. Brandon McKinzie et al. [MM1: Methods, Analysis & Insights from Multimodal LLM Pre-training](https://arxiv.org/abs/2403.09611). *arXiv preprint arXiv:2403.09611*.
- 2024\. Haotian Liu et al. [Improved Baselines with Visual Instruction Tuning](https://arxiv.org/abs/2310.03744). *IEEE/CVF Conference on Computer Vision and Pattern Recognition*.
- 2024\. Patrick Esser et al. [Scaling Rectified Flow Transformers for High-Resolution Image Synthesis](https://arxiv.org/abs/2403.03206). *International Conference on Machine Learning*.
- 2024\. Alec Radford et al. [Robust Speech Recognition via Large-Scale Weak Supervision](https://arxiv.org/abs/2212.04356). *International Conference on Machine Learning*.
- 2024\. Gemini Team. [Gemini 1.5: Unlocking Multimodal Understanding across Millions of Tokens of Context](https://storage.googleapis.com/deepmind-media/gemini/gemini_v1_5_report.pdf). *Google DeepMind Technical Report*.
- 2024\. J. Lu, C. Clark, et al. [Unified-IO 2: Scaling Autoregressive Multimodal Models with Vision, Language, Audio, and Action](https://openaccess.thecvf.com/content/CVPR2024/html/Lu_Unified-IO_2_Scaling_Autoregressive_Multimodal_Models_with_Vision_Language_Audio_CVPR_2024_paper.html). *CVPR*.
- 2024\. J. Zhan, J. Dai, et al. [AnyGPT: Unified Multimodal LLM with Discrete Sequence Modeling](https://aclanthology.org/2024.acl-long.521/). *ACL*.
- 2024\. Microsoft. [Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone](https://arxiv.org/abs/2404.14219). *arXiv preprint arXiv:2404.14219*.
- 2024\. Peng Wang et al. [Qwen2-VL: Enhancing Vision-Language Model's Perception of the World at Any Resolution](https://arxiv.org/abs/2409.12191). *arXiv preprint arXiv:2409.12191*.
- 2024\. Roman Bachmann et al. [4M-21: An Any-to-Any Vision Model for Tens of Tasks and Modalities](https://proceedings.neurips.cc/paper_files/paper/2024/hash/71883294314045d60c900113a359934b-Abstract-Conference.html). *NeurIPS*.
- 2024\. Zhuoyi Yang et al. [CogVideoX: Text-to-Video Diffusion Models with An Expert Transformer](https://arxiv.org/abs/2408.06072). *arXiv preprint arXiv:2408.06072*.
- 2024\. Shengbang Tong et al. [Cambrian-1: A Fully Open, Vision-Centric Exploration of Multimodal LLMs](https://arxiv.org/abs/2406.16860). *NeurIPS*.
- 2024\. Shukang Yin et al. [A Survey on Multimodal Large Language Models](https://doi.org/10.1093/nsr/nwae403). *National Science Review*.
- 2024\. Team, Chameleon. [Chameleon: Mixed-modal early-fusion foundation models](https://arxiv.org/abs/2405.09818). *arXiv*.
- 2024\. Y. Jin, K. Xu, et al. [Unified Language-Vision Pretraining in LLM with Dynamic Discrete Visual Tokenization](https://openreview.net/forum?id=Y1yARvAjc7). *ICLR*.
- 2024\. Yunze Ge et al. [SEED: Planting a SEED of Vision in Large Language Model](https://openreview.net/forum?id=lmCh0aACLi). *ICLR*.
- 2025\. Baidu ERNIE Team. [ERNIE 4.5 Technical Report](https://ernie.baidu.com/blog/publication/ERNIE_Technical_Report.pdf). *Baidu Technical Report*.
- 2025\. Gemma Team. [Gemma 3 Technical Report](https://arxiv.org/abs/2503.19786). *arXiv preprint arXiv:2503.19786*.
- 2025\. Qwen Team. [Qwen2.5-VL Technical Report](https://arxiv.org/abs/2502.13923). *arXiv preprint arXiv:2502.13923*.
- 2025\. Seed Team. [Seed1.5-VL Technical Report](https://arxiv.org/abs/2505.07062). *arXiv preprint arXiv:2505.07062*.

## 2.1 DNA and RNA

- 2021\. Yanrong Ji, Zhihan Zhou, Han Liu, Ramana V. Davuluri. [DNABERT: Pre-Trained Bidirectional Encoder Representations from Transformers Model for DNA-Language in Genome](https://doi.org/10.1093/bioinformatics/btab083). *Bioinformatics*.
- 2023\. Eric Nguyen, Michael Poli, Matthew G. Durrant, Armin W. Thomas, Brian Hie, Stefano Ermon, Christopher Re. [HyenaDNA: Long-Range Genomic Sequence Modeling at Single Nucleotide Resolution](https://arxiv.org/abs/2306.15794). *arXiv preprint arXiv:2306.15794*.
- 2025\. Hugo Dalla-Torre et al. [Nucleotide Transformer: Building and Evaluating Robust Foundation Models for Human Genomics](https://www.nature.com/articles/s41592-024-02523-z). *Nature Methods*.
- 2023\. Maxim Zvyagin et al. [GenSLMs: Genome-Scale Language Models Reveal SARS-CoV-2 Evolutionary Dynamics](https://journals.sagepub.com/doi/10.1177/10943420231201154). *The International Journal of High Performance Computing Applications*.
- 2023\. Zhihan Zhou et al. [DNABERT-2: Efficient Foundation Model and Benchmark for Multi-Species Genome](https://arxiv.org/abs/2306.15006). *arXiv preprint arXiv:2306.15006*.
- 2024\. Carlos Outeiral and Charlotte M. Deane. [Codon Language Embeddings Provide Strong Signals for Use in Protein Engineering](https://www.nature.com/articles/s42256-024-00791-0). *Nature Machine Intelligence*.
- 2024\. Eric Nguyen et al. [Sequence Modeling and Design from Molecular to Genome Scale with Evo](https://doi.org/10.1126/science.ado9336). *Science*.
- 2024\. Jan Christian Dietrich et al. [DNA Language Model GROVER Learns Sequence Context in the Human Genome](https://www.nature.com/articles/s42256-024-00872-0). *Nature Machine Intelligence*.
- 2024\. Yair Schiff et al. [Caduceus: Bi-Directional Equivariant Long-Range DNA Sequence Modeling](https://arxiv.org/abs/2403.03234). *ICML*.
- 2022\. Jiayang Chen et al. [Interpretable RNA Foundation Model from Unannotated Data for Highly Accurate RNA Structure and Function Predictions](https://arxiv.org/abs/2204.00300). *arXiv preprint arXiv:2204.00300*.
- 2024\. Chai Discovery Team et al. [Chai-1: Decoding the Molecular Interactions of Life](https://www.biorxiv.org/content/10.1101/2024.10.10.615955v2). *bioRxiv*.
- 2024\. Jeremy Wohlwend et al. [Boltz-1: Democratizing Biomolecular Interaction Modeling](https://www.biorxiv.org/content/10.1101/2024.11.19.624167v4). *bioRxiv*.
- 2025\. ByteDance AI Lab. [Protenix: Advancing Structure Prediction Through a Comprehensive AlphaFold3 Reproduction](https://openreview.net/forum?id=rdupZxS99R). *International Conference on Learning Representations*.
- 2025\. Gabriele Corso et al. [Boltz-2: Towards Accurate and Efficient Binding Affinity Prediction](https://www.biorxiv.org/content/10.1101/2025.06.14.659707v1). *bioRxiv*.
- 2025\. Eric Wang et al. [TxGemma: Efficient and Agentic LLMs for Therapeutics](https://arxiv.org/abs/2504.06196). *arXiv preprint arXiv:2504.06196*.
- 2025\. Conrad Testagrose and Christina Boucher. [Tokenization and Deep Learning Architectures in Genomics: A Comprehensive Review](https://doi.org/10.1016/j.csbj.2025.07.038). *Computational and Structural Biotechnology Journal*.
- 2025\. Haonan Feng et al. [Benchmarking DNA Foundation Models for Genomic and Genetic Tasks](https://www.nature.com/articles/s41467-025-65823-8). *Nature Communications*.
- 2025\. LeAnn M. Lindsey. [The Impact of Tokenizer Selection in Genomic Language Models](https://academic.oup.com/bioinformatics/article/41/9/btaf456/8237360). *Bioinformatics*.
- 2025\. Veniamin Fishman et al. [GENA-LM: A Family of Open-Source Foundational DNA Language Models for Long Sequences](https://academic.oup.com/nar/article/53/2/gkae1310/7954523). *Nucleic Acids Research*.
- 2025\. Yong He et al. [Generalized Biological Foundation Model with Unified Nucleic Acid and Protein Language](https://www.nature.com/articles/s42256-025-01044-4). *Nature Machine Intelligence*.
- 2026\. Gregory Brixi et al. [Genome Modelling and Design Across All Domains of Life with Evo 2](https://doi.org/10.1038/s41586-026-10176-5). *Nature*.

## 2.2 Proteins and Peptides

- 2021\. Ahmed Elnaggar et al. [ProtTrans: Toward Cracking the Language of Life's Code Through Self-Supervised Deep Learning and High Performance Computing](https://doi.org/10.1109/TPAMI.2021.3095381). *IEEE Transactions on Pattern Analysis and Machine Intelligence*.
- 2021\. Alexander Rives et al. [Biological Structure and Function Emerge from Scaling Unsupervised Learning to 250 Million Protein Sequences](https://doi.org/10.1073/pnas.2016239118). *Proceedings of the National Academy of Sciences*.
- 2022\. Nadav Brandes, Dan Ofer, Yam Peleg, Nadav Rappoport, Michal Linial. [ProteinBERT: A Universal Deep-Learning Model of Protein Sequence and Function](https://doi.org/10.1093/bioinformatics/btac020). *Bioinformatics*.
- 2023\. Ali Madani et al. [Large Language Models Generate Functional Protein Sequences Across Diverse Families](https://doi.org/10.1038/s41587-022-01618-2). *Nature Biotechnology*.
- 2023\. Ruochi Zhang et al. [PepLand: A Large-Scale Pre-Trained Peptide Representation Model for a Comprehensive Landscape of Both Canonical and Non-Canonical Amino Acids](https://arxiv.org/abs/2311.04419). *arXiv preprint arXiv:2311.04419*.
- 2023\. Tianlai Chen et al. [PepMLM: Target Sequence-Conditioned Generation of Therapeutic Peptide Binders via Span Masked Language Modeling](https://arxiv.org/abs/2310.03842). *arXiv preprint arXiv:2310.03842*.
- 2023\. Zeming Lin et al. [Evolutionary-Scale Prediction of Atomic-Level Protein Structure with a Language Model](https://doi.org/10.1126/science.ade2574). *Science*.
- 2024\. Andrew Liu, Axel Elaldi, Nathan Russell, and Olivia Viessmann. [Bio2Token: All-Atom Tokenization of Any Biomolecular Structure with Mamba](https://arxiv.org/abs/2410.19110). *arXiv preprint arXiv:2410.19110*.
- 2024\. Jiahan Li, Chaoran Cheng, Zuofan Wu, Ruihan Guo, Shitong Luo, Zhizhou Ren, Jian Peng, and Jianzhu Ma. [Full-Atom Peptide Design based on Multi-modal Flow Matching](https://proceedings.mlr.press/v235/li24o.html) (PepFlow). *International Conference on Machine Learning*.
- 2024\. Xiangzhe Kong, Yinjun Jia, Wenbing Huang, and Yang Liu. [Full-Atom Peptide Design with Geometric Latent Diffusion](https://arxiv.org/abs/2402.13555). *Advances in Neural Information Processing Systems*.
- 2024\. Haitao Lin, Odin Zhang, Huifeng Zhao, Dejun Jiang, Lirong Wu, Zicheng Liu, Yufei Huang, and Stan Z. Li. [PPFLOW: Target-Aware Peptide Design with Torsional Flow Matching](https://proceedings.mlr.press/v235/lin24z.html). *International Conference on Machine Learning*.
- 2024\. Benoit Gaujac et al. [Learning the Language of Protein Structure](https://arxiv.org/abs/2405.15840). *arXiv*.
- 2024\. Jin Su et al. [SaProt: Protein Language Modeling with Structure-Aware Vocabulary](https://openreview.net/forum?id=6MRm3G4NiU). *International Conference on Learning Representations*.
- 2024\. Josh Abramson et al. [Accurate Structure Prediction of Biomolecular Interactions with AlphaFold 3](https://www.nature.com/articles/s41586-024-07487-w). *Nature*.
- 2024\. Michael Heinzinger et al. [Bilingual Language Model for Protein Sequence and Structure](https://academic.oup.com/nargab/article/6/4/lqae150/7901286). *NAR Genomics and Bioinformatics*.
- 2024\. Michel van Kempen et al. [Fast and Accurate Protein Structure Search with Foldseek](https://doi.org/10.1038/s41587-023-01773-0). *Nature Biotechnology*.
- 2024\. Michelle M. Li et al. [Contextual AI Models for Single-Cell Protein Biology](https://doi.org/10.1038/s41592-024-02341-3). *Nature Methods*.
- 2024\. Osama Abdin and Philip M. Kim. [Direct Conformational Sampling from Peptide Energy Landscapes through Hypernetwork-Conditioned Diffusion](https://www.nature.com/articles/s42256-024-00860-4). *Nature Machine Intelligence*.
- 2024\. Owen Queen et al. [A Multimodal Foundation Model for Protein Phenotypes](https://zitniklab.hms.harvard.edu/ProCyon/). *bioRxiv*.
- 2024\. Tong Wang et al. [Ab Initio Characterization of Protein Molecular Dynamics with AI2BMD](https://www.nature.com/articles/s41586-024-08127-z). *Nature*.
- 2024\. Xiaopeng Xu et al. [HELM-GPT: De Novo Macrocyclic Peptide Design Using Generative Pre-Trained Transformer](https://doi.org/10.1093/bioinformatics/btae364). *Bioinformatics*.
- 2024\. Xinyou Wang et al. [DPLM-2: A Multimodal Diffusion Protein Language Model](https://arxiv.org/abs/2410.13782). *arXiv*.
- 2024\. Zhangyang Gao et al. [FoldToken: Learning Protein Language via Vector Quantization and Beyond](https://arxiv.org/abs/2403.09673). *arXiv*.
- 2024\. Zhangyang Gao, Cheng Tan, and Stan Z. Li. [FoldToken2: Learning Compact, Invariant and Generative Protein Structure Language](https://arxiv.org/abs/2407.00050). *arXiv*.
- 2024\. Chai Discovery Team et al. [Chai-1: Decoding the Molecular Interactions of Life](https://www.biorxiv.org/content/10.1101/2024.10.10.615955v2). *bioRxiv*.
- 2024\. Jeremy Wohlwend et al. [Boltz-1: Democratizing Biomolecular Interaction Modeling](https://www.biorxiv.org/content/10.1101/2024.11.19.624167v4). *bioRxiv*.
- 2025\. ByteDance AI Lab. [Protenix: Advancing Structure Prediction Through a Comprehensive AlphaFold3 Reproduction](https://openreview.net/forum?id=rdupZxS99R). *International Conference on Learning Representations*.
- 2025\. Gabriele Corso et al. [Boltz-2: Towards Accurate and Efficient Binding Affinity Prediction](https://www.biorxiv.org/content/10.1101/2025.06.14.659707v1). *bioRxiv*.
- 2025\. Eric Wang et al. [TxGemma: Efficient and Agentic LLMs for Therapeutics](https://arxiv.org/abs/2504.06196). *arXiv preprint arXiv:2504.06196*.
- 2025\. Thomas Hayes et al. [Simulating 500 Million Years of Evolution with a Language Model](https://doi.org/10.1126/science.ads0018). *Science*.
- 2025\. Xinyu Yuan et al. [Protein Structure Tokenization: Benchmarking and New Recipe](https://proceedings.mlr.press/v267/yuan25i.html). *International Conference on Machine Learning*.
- 2025\. Zijing Liu, Bin Feng, He Cao, and Yu Li. [From Static Structures to Ensembles: Studying and Harnessing Protein Structure Tokenization](https://arxiv.org/abs/2511.10056). *NeurIPS AI for Science Workshop*.
- 2026\. Kaiwen Shi and Carlos Oliver. [ENSEMBITS: An Alphabet of Protein Conformational Ensembles](https://arxiv.org/abs/2605.13789). *arXiv preprint arXiv:2605.13789*.
- 2026\. Michael Sun, Weize Yuan, Gang Liu, Wojciech Matusik, Marinka Zitnik. [Protein Structure Tokenization via Geometric Byte Pair Encoding](https://arxiv.org/abs/2511.11758). *International Conference on Learning Representations*.
- 2026\. Rohit Dilip, Evan Zhang, Ayush Varshney, and David Van Valen. [Flow Autoencoders Are Effective Protein Tokenizers](https://openreview.net/forum?id=5p9uled7JM). *International Conference on Learning Representations*.
- 2026\. Biohub. [Language Modeling Materializes a World Model of Protein Biology](https://biohub.ai/papers/esm_protein.pdf). *Preprint*.

## 2.3 Molecules and Reactions

- 1988\. David Weininger. [SMILES, a Chemical Language and Information System. 1. Introduction to Methodology and Encoding Rules](https://doi.org/10.1021/ci00057a005). *Journal of Chemical Information and Computer Sciences*.
- 2015\. Stephen R. Heller et al. [InChI, the IUPAC International Chemical Identifier](https://doi.org/10.1186/s13321-015-0068-4). *Journal of Cheminformatics*.
- 2018\. Noel O'Boyle and Andrew Dalke. [DeepSMILES: An Adaptation of SMILES for Use in Machine-Learning of Chemical Structures](https://www.cambridge.org/engage/chemrxiv/article-details/60c73ed6567dfe7e5fec388d). *ChemRxiv*.
- 2018\. Wengong Jin, Regina Barzilay, Tommi Jaakkola. [Junction Tree Variational Autoencoder for Molecular Graph Generation](https://proceedings.mlr.press/v80/jin18a.html). *International Conference on Machine Learning*.
- 2020\. Mario Krenn, Florian Hase, AkshatKumar Nigam, Pascal Friederich, Alan Aspuru-Guzik. [Self-Referencing Embedded Strings: A 100 Percent Robust Molecular String Representation](https://doi.org/10.1088/2632-2153/aba947). *Machine Learning: Science and Technology*.
- 2020\. Seyone Chithrananda, Gabriel Grand, and Bharath Ramsundar. [ChemBERTa: Large-Scale Self-Supervised Pretraining for Molecular Property Prediction](https://arxiv.org/abs/2010.09885). *arXiv*.
- 2020\. Wengong Jin, Regina Barzilay, and Tommi Jaakkola. [Hierarchical Generation of Molecular Graphs Using Structural Motifs](https://proceedings.mlr.press/v119/jin20a.html). *International Conference on Machine Learning*.
- 2021\. Xinhao Li and Denis Fourches. [SMILES Pair Encoding: A Data-Driven Substructure Tokenization Algorithm for Deep Learning](https://pubs.acs.org/doi/10.1021/acs.jcim.0c01127). *Journal of Chemical Information and Modeling*.
- 2022\. Xiangzhe Kong et al. [Molecule Generation by Principal Subgraph Mining and Assembling](https://proceedings.neurips.cc/paper_files/paper/2022/hash/1160792eab11de2bbaf9e71fce191e8c-Abstract-Conference.html). *Advances in Neural Information Processing Systems*.
- 2023\. Gengmo Zhou et al. [Uni-Mol: A Universal 3D Molecular Representation Learning Framework](https://openreview.net/forum?id=6K2RM6wVqKu). *International Conference on Learning Representations*.
- 2023\. Umit V. Ucak, Islambek Ashyrmamatov, and Juyong Lee. [Improving the Quality of Chemical Language Model Outcomes with Atom-in-SMILES Tokenization](https://doi.org/10.1186/s13321-023-00725-9). *Journal of Cheminformatics*.
- 2022\. Jerret Ross et al. [Large-Scale Chemical Language Representations Capture Molecular Structure and Properties](https://www.nature.com/articles/s42256-022-00580-7). *Nature Machine Intelligence*.
- 2024\. Gang Liu, Eric Inae, Tong Zhao, Meng Jiang. [Graph Diffusion Transformers for Multi-Conditional Molecular Generation](https://arxiv.org/abs/2401.13858). *Advances in Neural Information Processing Systems*.
- 2024\. Jinho Chang and Jong Chul Ye. [Bidirectional Generation of Structure and Properties Through a Single Molecular Foundation Model](https://www.nature.com/articles/s41467-024-46440-3). *Nature Communications*.
- 2024\. Wei Feng et al. [Generation of 3D Molecules in Pockets via a Language Model](https://www.nature.com/articles/s42256-023-00775-6). *Nature Machine Intelligence*.
- 2024\. Chai Discovery Team et al. [Chai-1: Decoding the Molecular Interactions of Life](https://www.biorxiv.org/content/10.1101/2024.10.10.615955v2). *bioRxiv*.
- 2024\. Jeremy Wohlwend et al. [Boltz-1: Democratizing Biomolecular Interaction Modeling](https://www.biorxiv.org/content/10.1101/2024.11.19.624167v4). *bioRxiv*.
- 2024\. Yuchen Shen and Barnabás Póczos. [GraphBPE: Molecular Graphs Meet Byte-Pair Encoding](https://arxiv.org/abs/2407.19039). *ICML AI for Science Workshop*.
- 2025\. Gang Liu et al. [Learning Molecular Representation in a Cell](https://openreview.net/forum?id=BbZy8nI1si). *International Conference on Learning Representations*.
- 2025\. Gang Liu, Michael Sun, Wojciech Matusik, Meng Jiang, Jie Chen. [Multimodal Large Language Models for Inverse Molecular Design with Retrosynthetic Planning](https://arxiv.org/abs/2410.04223). *International Conference on Learning Representations*.
- 2025\. Haotian Cui et al. [Towards Multimodal Foundation Models in Molecular Cell Biology](https://www.nature.com/articles/s41586-025-08710-y). *Nature*.
- 2025\. Jike Wang et al. [Token-Mol 1.0: Tokenized Drug Design with Large Language Models](https://www.nature.com/articles/s41467-025-59628-y). *Nature Communications*.
- 2025\. Michael Sun, Weize Yuan, Gang Liu, Wojciech Matusik, Jie Chen. [Foundation Molecular Grammar: Multi-Modal Foundation Models Induce Interpretable Molecular Graph Languages](https://arxiv.org/abs/2505.22948). *International Conference on Machine Learning*.
- 2025\. ByteDance AI Lab. [Protenix: Advancing Structure Prediction Through a Comprehensive AlphaFold3 Reproduction](https://openreview.net/forum?id=rdupZxS99R). *International Conference on Learning Representations*.
- 2025\. Brandon M. Wood et al. [UMA: A Family of Universal Models for Atoms](https://arxiv.org/abs/2506.23971). *arXiv preprint arXiv:2506.23971*.
- 2025\. Eric Wang et al. [TxGemma: Efficient and Agentic LLMs for Therapeutics](https://arxiv.org/abs/2504.06196). *arXiv preprint arXiv:2504.06196*.
- 2025\. Gabriele Corso et al. [Boltz-2: Towards Accurate and Efficient Binding Affinity Prediction](https://www.biorxiv.org/content/10.1101/2025.06.14.659707v1). *bioRxiv*.
- 2026\. Alexius Wadell, Anoushka Bhutani, and Venkatasubramanian Viswanathan. [Tokenization for Molecular Foundation Models](https://doi.org/10.1021/acs.jcim.5c01856). *Journal of Chemical Information and Modeling*.
- 2026\. Gang Liu, Jie Chen, Yihan Zhu, Michael Sun, Tengfei Luo, Nitesh V. Chawla, Meng Jiang. [Graph Diffusion Transformers Are In-Context Molecular Designers](https://arxiv.org/abs/2510.08744). *International Conference on Learning Representations*.
- 2026\. Xuan Liu et al. [Bridging Three-Dimensional Molecular Structures and Artificial Intelligence with a Conformation Description Language](https://www.nature.com/articles/s42256-026-01250-8). *Nature Machine Intelligence*.
- 2026\. Chen Yang et al. [A Large-Scale Foundation Model Enables Simulation-to-Real Adaptation for Nuclear Magnetic Resonance-Based Molecular Structure Analysis](https://arxiv.org/abs/2606.20756). *arXiv preprint arXiv:2606.20756*.

## 2.4 Crystals, Materials, and Polymers

- 2017\. Kristof T. Schuett et al. [SchNet: A Continuous-Filter Convolutional Neural Network for Modeling Quantum Interactions](https://proceedings.neurips.cc/paper/2017/hash/303ed4c69846ab36c2904d3ba8573050-Abstract.html). *Advances in Neural Information Processing Systems*.
- 2018\. Tian Xie and Jeffrey C. Grossman. [Crystal Graph Convolutional Neural Networks for an Accurate and Interpretable Prediction of Material Properties](https://doi.org/10.1103/PhysRevLett.120.145301). *Physical Review Letters*.
- 2019\. Chi Chen et al. [Graph Networks as a Universal Machine Learning Framework for Molecules and Crystals](https://doi.org/10.1021/acs.chemmater.9b01294). *Chemistry of Materials*.
- 2019\. Tingyi Lin et al. [BigSMILES: A Structurally-Based Line Notation for Describing Macromolecules](https://doi.org/10.1021/acscentsci.9b00476). *ACS Central Science*.
- 2021\. Kamal Choudhary and Brian DeCost. [Atomistic Line Graph Neural Network for Improved Materials Property Predictions](https://doi.org/10.1038/s41524-021-00650-1). *npj Computational Materials*.
- 2022\. Chi Chen and Shyue Ping Ong. [A Universal Graph Deep Learning Interatomic Potential for the Periodic Table](https://doi.org/10.1038/s43588-022-00349-3). *Nature Computational Science*.
- 2023\. Changwen Xu et al. [TransPolymer: A Transformer-Based Language Model for Polymer Property Predictions](https://doi.org/10.1038/s41524-023-01016-5). *npj Computational Materials*.
- 2023\. Christopher Kuenneth, Rampi Ramprasad. [polyBERT: A Chemical Language Model for Fully Machine-Driven Ultrafast Polymer Informatics](https://doi.org/10.1038/s41467-023-39868-6). *Nature Communications*.
- 2024\. Benjamin Kurt Miller et al. [FlowLLM: Flow Matching for Material Generation with Large Language Models as Base Distributions](https://proceedings.neurips.cc/paper_files/paper/2024/hash/51d317df78eded9eb3c9d3fb1091c279-Abstract-Conference.html). *Advances in Neural Information Processing Systems*.
- 2024\. Han Yang et al. [MatterSim: A Deep Learning Atomistic Model Across Elements, Temperatures and Pressures](https://arxiv.org/abs/2405.04967). *arXiv preprint arXiv:2405.04967*.
- 2024\. Luis Barroso-Luque et al. [Open Materials 2024 Inorganic Materials Dataset and Models](https://arxiv.org/abs/2410.12771). *arXiv preprint arXiv:2410.12771*.
- 2024\. Luis M. Antunes et al. [Crystal Structure Generation with Autoregressive Large Language Modeling](https://doi.org/10.1038/s41467-024-54639-7). *Nature Communications*.
- 2024\. Tatsunori Taniai, Ryo Igarashi, Yoshitaka Ushiku, Kanta Ono. [Crystalformer: Infinitely Connected Attention for Periodic Structure Encoding](https://openreview.net/forum?id=fxQiecl9HB). *International Conference on Learning Representations*.
- 2025\. Amil Merchant et al. [Foundation Models for Materials Discovery: Current State and Future Directions](https://doi.org/10.1038/s41524-025-01538-0). *npj Computational Materials*.
- 2025\. Claudio Zeni et al. [A Generative Model for Inorganic Materials Design](https://doi.org/10.1038/s41586-025-08628-5). *Nature*.
- 2025\. Brandon M. Wood et al. [UMA: A Family of Universal Models for Atoms](https://arxiv.org/abs/2506.23971). *arXiv preprint arXiv:2506.23971*.
- 2025\. Fanmeng Wang, Shan Mei, Wentao Guo, Hongshuai Wang, Qi Ou, Zhifeng Gao, and Hongteng Xu. [Unifying Polymer Modeling and Design via a Conformation-Centric Generative Foundation Model](https://arxiv.org/abs/2510.16023). *arXiv preprint arXiv:2510.16023*.
- 2025\. Fanmeng Wang, Wentao Guo, Qi Ou, Hongshuai Wang, Haitao Lin, Hongteng Xu, and Zhifeng Gao. [PolyConf: Unlocking Polymer Conformation Generation through Hierarchical Generative Models](https://proceedings.mlr.press/v267/wang25ah.html). *International Conference on Machine Learning*.
- 2025\. Yihan Zhu, Gang Liu, Eric Inae, Tengfei Luo, Meng Jiang. [Learning Repetition-Invariant Representations for Polymer Informatics](https://arxiv.org/abs/2505.10726). *Advances in Neural Information Processing Systems*.
- 2026\. Dhruv Ahlawat et al. [A Family of Large Language Models for Materials Research with Insights into Model Adaptability in Continued Pretraining](https://doi.org/10.1038/s42256-026-01199-8). *Nature Machine Intelligence*.
- 2026\. Eric C.-Y. Yuan et al. [Foundation Models for Atomistic Simulation of Chemistry and Materials](https://www.nature.com/articles/s41570-025-00793-5). *Nature Reviews Chemistry*.
- 2026\. Rui Jiao et al. [An Equivariant Pretrained Transformer for Unified 3D Molecular Representation Learning](https://doi.org/10.1038/s41467-026-69185-7). *Nature Communications*.

## 2.5 Spectra and Microscopy

- 2021\. Florian Huber et al. [MS2DeepScore: A Novel Deep Learning Similarity Measure to Compare Tandem Mass Spectra](https://doi.org/10.1186/s13321-021-00558-4). *Journal of Cheminformatics*.
- 2021\. Florian Huber et al. [Spec2Vec: Improved Mass Spectral Similarity Scoring through Learning of Structural Relationships](https://doi.org/10.1371/journal.pcbi.1008724). *PLOS Computational Biology*.
- 2024\. Melih Yilmaz et al. [Sequence-to-Sequence Translation from Mass Spectra to Peptides with a Transformer Model](https://www.nature.com/articles/s41467-024-49731-x). *Nature Communications*.
- 2025\. Kevin Eloff et al. [InstaNovo Enables Diffusion-Powered de Novo Peptide Sequencing in Large-Scale Proteomics Experiments](https://www.nature.com/articles/s42256-025-01019-5). *Nature Machine Intelligence*.
- 2025\. Roman Bushuiev et al. [Self-Supervised Learning of Molecular Representations from Millions of Tandem Mass Spectra Using DreaMS](https://www.nature.com/articles/s41587-025-02663-3). *Nature Biotechnology*.
- 2025\. Yang Xu et al. [A Large Language Model for Deriving Spectral Embeddings for Accurate Compound Identification in Mass Spectrometry](https://www.nature.com/articles/s42004-025-01708-7). *Communications Chemistry*.
- 2026\. Chen Yang et al. [A Large-Scale Foundation Model Enables Simulation-to-Real Adaptation for Nuclear Magnetic Resonance-Based Molecular Structure Analysis](https://arxiv.org/abs/2606.20756). *arXiv preprint arXiv:2606.20756*.

## 2.6 Medical Imaging and Digital Pathology

- 2024\. Ming Y. Lu et al. [A Visual-Language Foundation Model for Computational Pathology](https://doi.org/10.1038/s41591-024-02856-4). *Nature Medicine*.
- 2024\. Richard J. Chen et al. [Towards a General-Purpose Foundation Model for Computational Pathology](https://doi.org/10.1038/s41591-024-02857-3). *Nature Medicine*.
- 2024\. Hanwen Xu et al. [A Whole-Slide Foundation Model for Digital Pathology from Real-World Data](https://www.nature.com/articles/s41586-024-07441-w). *Nature*.
- 2024\. Eric Zimmermann et al. [Virchow2: Scaling Self-Supervised Mixed Magnification Models in Pathology](https://arxiv.org/abs/2408.00738). *arXiv preprint arXiv:2408.00738*.
- 2026\. Andrew Sellergren et al. [MedGemma 1.5 Technical Report](https://arxiv.org/abs/2604.05081). *arXiv preprint arXiv:2604.05081*.
- 2026\. Marin Scalbert et al. [H-optimus-1: A Foundation Model for Computational Histopathology](https://doi.org/10.1158/1538-7445.AM2026-LB174). *Cancer Research*.

## 2.7 Omics and Cells

- 2022\. Fan Yang et al. [scBERT as a Large-Scale Pretrained Deep Language Model for Cell Type Annotation of Single-Cell RNA-seq Data](https://doi.org/10.1038/s42256-022-00534-z). *Nature Machine Intelligence*.
- 2023\. Christina V. Theodoris et al. [Transfer Learning Enables Predictions in Network Biology](https://doi.org/10.1038/s41586-023-06139-9). *Nature*.
- 2024\. Charlotte Bunne et al. [How to Build the Virtual Cell with Artificial Intelligence: Priorities and Opportunities](https://doi.org/10.1016/j.cell.2024.11.015). *Cell*.
- 2024\. Haotian Cui et al. [scGPT: Toward Building a Foundation Model for Single-Cell Multi-Omics Using Generative AI](https://doi.org/10.1038/s41592-024-02201-0). *Nature Methods*.
- 2025\. Fan Zhang et al. [A Survey on Foundation Language Models for Single-Cell Biology](https://aclanthology.org/2025.acl-long.26/). *Proceedings of ACL*.
- 2025\. Seungbeom Kim et al. [Single-Cell Foundation Models: Bringing Artificial Intelligence into Cell Biology](https://doi.org/10.1038/s12276-025-01547-5). *Experimental and Molecular Medicine*.
- 2026\. Yanay Rosen et al. [Universal Cell Embedding Provides a Foundation Model for Cell Biology](https://doi.org/10.1038/s41586-026-10689-z). *Nature*.
- 2025\. Abhinav K. Adduri et al. [Predicting Cellular Responses to Perturbation Across Diverse Contexts with State](https://www.biorxiv.org/content/10.1101/2025.06.26.661135v1). *bioRxiv*.
- 2026\. Mingze Dong et al. [Stack: In-Context Learning of Single-Cell Biology](https://doi.org/10.64898/2026.01.09.698608). *bioRxiv*.

## 2.8 Physical Fields and Simulations

- 2021\. Michael M. Bronstein, Joan Bruna, Taco Cohen, Petar Velickovic. [Geometric Deep Learning: Grids, Groups, Graphs, Geodesics, and Gauges](https://arxiv.org/abs/2104.13478). *arXiv preprint arXiv:2104.13478*.
- 2021\. Tobias Pfaff et al. [Learning Mesh-Based Simulation with Graph Networks](https://openreview.net/forum?id=roNqYL0_XP). *International Conference on Learning Representations*.
- 2023\. Nikola Kovachki, Zongyi Li, Burigede Liu, Kamyar Azizzadenesheli, Kaushik Bhattacharya, Andrew Stuart, and Anima Anandkumar. [Neural Operator: Learning Maps Between Function Spaces With Applications to PDEs](https://www.jmlr.org/papers/v24/21-1524.html). *Journal of Machine Learning Research*.
- 2024\. Haixu Wu et al. [Transolver: A Fast Transformer Solver for PDEs on General Geometries](https://proceedings.mlr.press/v235/wu24r.html). *International Conference on Machine Learning*.
- 2025\. Benjamin Holzschuh, Qiang Liu, Georg Kohl, and Nils Thuerey. [PDE-Transformer: Efficient and Versatile Transformers for Physics Simulations](https://proceedings.mlr.press/v267/holzschuh25a.html). *International Conference on Machine Learning*.
- 2025\. Palash Bera and Jagannath Mondal. [Accurate Prediction of the Kinetic Sequence of Physicochemical States Using Generative Artificial Intelligence](https://doi.org/10.1039/D5SC00108K). *Chemical Science*.
- 2025\. Yiqing Shen, Hao Ding, Lalithkumar Seenivasan, Tianmin Shu, and Mathias Unberath. [Position: Foundation Models Need Digital Twin Representations](https://arxiv.org/abs/2505.03798). *arXiv preprint arXiv:2505.03798*.

## 2.9 Earth System Observations

- 2022\. Jaideep Pathak et al. [FourCastNet: A Global Data-Driven High-Resolution Weather Model Using Adaptive Fourier Neural Operators](https://arxiv.org/abs/2202.11214). *arXiv preprint arXiv:2202.11214*.
- 2022\. Zhihan Gao et al. [Earthformer: Exploring Space-Time Transformers for Earth System Forecasting](https://arxiv.org/abs/2207.05833). *Advances in Neural Information Processing Systems*.
- 2023\. Kaifeng Bi et al. [Accurate Medium-Range Global Weather Forecasting with 3D Neural Networks](https://doi.org/10.1038/s41586-023-06185-3). *Nature*.
- 2023\. Remi Lam et al. [Learning Skillful Medium-Range Global Weather Forecasting](https://doi.org/10.1126/science.adi2336). *Science*.
- 2023\. Tung Nguyen et al. [ClimaX: A Foundation Model for Weather and Climate](https://proceedings.mlr.press/v202/nguyen23a.html). *International Conference on Machine Learning*.
- 2024\. Ilan Price et al. [Probabilistic Weather Forecasting with Machine Learning](https://doi.org/10.1038/s41586-024-08252-9). *Nature*.
- 2024\. Stephan Hoyer et al. [Neural General Circulation Models for Weather and Climate](https://doi.org/10.1038/s41586-024-07744-y). *Nature*.
- 2025\. Cristian Bodnar et al. [A Foundation Model for the Earth System](https://www.nature.com/articles/s41586-025-09005-y). *Nature*.
- 2024\. Daniela Szwarcman et al. [Prithvi-EO-2.0: A Versatile Multi-Temporal Foundation Model for Earth Observation Applications](https://arxiv.org/abs/2412.02732). *arXiv preprint arXiv:2412.02732*.
- 2024\. Johannes Schmude et al. [Prithvi WxC: Foundation Model for Weather and Climate](https://arxiv.org/abs/2409.13598). *arXiv preprint arXiv:2409.13598*.
- 2025\. Johannes Jakubik et al. [TerraMind: Large-Scale Generative Multimodality for Earth Observation](https://arxiv.org/abs/2504.11171). *arXiv preprint arXiv:2504.11171*.

## 3. Theoretical and Method Foundations for Future Tokenizers

> This section records papers that define useful criteria for tokenizers and earlier methods that can form units, even when the authors did not use the term *tokenizer*.

- 1949\. Claude E. Shannon. [Communication in the Presence of Noise](https://ieeexplore.ieee.org/document/1697831). *Proceedings of the IRE*.
- 1959\. Claude E. Shannon. [Coding Theorems for a Discrete Source With a Fidelity Criterion](https://ieeexplore.ieee.org/document/5311476). *IRE National Convention Record*.
- 1963\. G. N. Ramachandran, C. Ramakrishnan, and V. Sasisekharan. [Stereochemistry of Polypeptide Chain Configurations](https://doi.org/10.1016/S0022-2836(63)80023-6). *Journal of Molecular Biology*.
- 1978\. Jorma Rissanen. [Modeling by Shortest Data Description](https://doi.org/10.1016/0005-1098(78)90005-5). *Automatica*.
- 1983\. Wolfgang Kabsch and Christian Sander. [Dictionary of Protein Secondary Structure: Pattern Recognition of Hydrogen-Bonded and Geometrical Features](https://doi.org/10.1002/bip.360221211). *Biopolymers*.
- 1987\. Irving Biederman. [Recognition-by-Components: A Theory of Human Image Understanding](https://doi.org/10.1037/0033-295X.94.2.115). *Psychological Review*.
- 1989\. Stephane G. Mallat. [A Theory for Multiresolution Signal Decomposition: The Wavelet Representation](https://doi.org/10.1109/34.192463). *IEEE Transactions on Pattern Analysis and Machine Intelligence*.
- 1996\. Guy W. Bemis and Mark A. Murcko. [The Properties of Known Drugs. 1. Molecular Frameworks](https://doi.org/10.1021/jm9602928). *Journal of Medicinal Chemistry*.
- 1999\. Naftali Tishby, Fernando C. Pereira, and William Bialek. [The Information Bottleneck Method](https://arxiv.org/abs/physics/0004057). *Allerton Conference on Communication, Control, and Computing*.
- 2000\. Jianbo Shi and Jitendra Malik. [Normalized Cuts and Image Segmentation](https://doi.org/10.1109/34.868688). *IEEE Transactions on Pattern Analysis and Machine Intelligence*.
- 2002\. Ron Milo et al. [Network Motifs: Simple Building Blocks of Complex Networks](https://doi.org/10.1126/science.298.5594.824). *Science*.
- 2004\. Pedro F. Felzenszwalb and Daniel P. Huttenlocher. [Efficient Graph-Based Image Segmentation](https://doi.org/10.1023/B:VISI.0000022288.19776.77). *International Journal of Computer Vision*.
- 2008\. Jorg Degen, Christof Wegscheid-Gerlach, Andrea Zaliani, and Matthias Rarey. [On the Art of Compiling and Using Drug-Like Chemical Fragment Spaces](https://doi.org/10.1002/cmdc.200800178). *ChemMedChem*.
- 2012\. Radhakrishna Achanta, Appu Shaji, Kevin Smith, Aurelien Lucchi, Pascal Fua, and Sabine Susstrunk. [SLIC Superpixels Compared to State-of-the-Art Superpixel Methods](https://doi.org/10.1109/TPAMI.2012.120). *IEEE Transactions on Pattern Analysis and Machine Intelligence*.
- 2016\. Taco S. Cohen and Max Welling. [Group Equivariant Convolutional Networks](https://proceedings.mlr.press/v48/cohenc16.html). *International Conference on Machine Learning*.
- 2017\. Manzil Zaheer et al. [Deep Sets](https://proceedings.neurips.cc/paper_files/paper/2017/hash/f22e4747da1aa27e363d86d40ff442fe-Abstract.html). *Advances in Neural Information Processing Systems*.
- 2018\. Peter W. Battaglia et al. [Relational Inductive Biases, Deep Learning, and Graph Networks](https://arxiv.org/abs/1806.01261). *arXiv preprint arXiv:1806.01261*.
- 2019\. Christopher P. Burgess et al. [MONet: Unsupervised Scene Decomposition and Representation](https://arxiv.org/abs/1901.11390). *arXiv preprint arXiv:1901.11390*.
- 2019\. Yochai Blau and Tomer Michaeli. [Rethinking Lossy Compression: The Rate-Distortion-Perception Tradeoff](https://proceedings.mlr.press/v97/blau19a.html). *International Conference on Machine Learning*.
- 2020\. Francesco Locatello et al. [Object-Centric Learning with Slot Attention](https://proceedings.neurips.cc/paper/2020/hash/8511df98c02ab60aea1b2356c013bc0f-Abstract.html). *Advances in Neural Information Processing Systems*.

## Public Hugging Face Models

Each model is assigned to one or more collection sections. The tokenizer classification refers only to token formation, rather than to the foundation model that consumes the tokens.

| Model | Collection Section | Tokenizer Classification | Sources |
|---|---|---|---|
| [Llama-3.1-8B-Instruct](https://huggingface.co/meta-llama/Llama-3.1-8B-Instruct) | 1.1 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2407.21783), [GitHub](https://github.com/meta-llama/llama-models) |
| [Qwen2.5-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct) | 1.1 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2412.15115), [GitHub](https://github.com/QwenLM/Qwen2.5) |
| [Qwen2.5-VL-7B-Instruct](https://huggingface.co/Qwen/Qwen2.5-VL-7B-Instruct) | 1.1, 1.2, 1.8 | Hybrid; sequential neural-algorithmic tokenization | [Paper](https://arxiv.org/abs/2502.13923), [GitHub](https://github.com/QwenLM/Qwen2.5-VL) |
| [LLaVA-1.5-7B](https://huggingface.co/llava-hf/llava-1.5-7b-hf) | 1.1, 1.2, 1.8 | Hybrid; composed tokenizer streams | [Paper](https://arxiv.org/abs/2310.03744), [GitHub](https://github.com/haotian-liu/LLaVA) |
| [FLUX.1-dev](https://huggingface.co/black-forest-labs/FLUX.1-dev) | 1.1, 1.2, 1.8 | Hybrid; composed tokenizer streams | [GitHub](https://github.com/black-forest-labs/flux) |
| [Stable Diffusion 3.5 Large](https://huggingface.co/stabilityai/stable-diffusion-3.5-large) | 1.1, 1.2, 1.8 | Hybrid; composed tokenizer streams | [Paper](https://arxiv.org/abs/2403.03206), [GitHub](https://github.com/Stability-AI/sd3.5) |
| [Whisper-large-v3](https://huggingface.co/openai/whisper-large-v3) | 1.1, 1.3, 1.8 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2212.04356), [GitHub](https://github.com/openai/whisper) |
| [EnCodec-32kHz](https://huggingface.co/facebook/encodec_32khz) | 1.3 | Neural; quantized latent tokens | [Paper](https://arxiv.org/abs/2210.13438), [GitHub](https://github.com/facebookresearch/encodec) |
| [MusicGen-large](https://huggingface.co/facebook/musicgen-large) | 1.1, 1.3, 1.8 | Hybrid; composed tokenizer streams | [Paper](https://arxiv.org/abs/2306.05284), [GitHub](https://github.com/facebookresearch/audiocraft) |
| [CogVideoX-5B](https://huggingface.co/zai-org/CogVideoX-5b) | 1.1, 1.2, 1.8 | Neural; continuous latent tokens | [Paper](https://arxiv.org/abs/2408.06072), [GitHub](https://github.com/THUDM/CogVideo) |
| [StarCoder2-7B](https://huggingface.co/bigcode/starcoder2-7b) | 1.1 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2402.19173), [GitHub](https://github.com/bigcode-project/starcoder2) |
| [SAM ViT-H](https://huggingface.co/facebook/sam-vit-huge) | 1.2 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2304.02643), [GitHub](https://github.com/facebookresearch/segment-anything) |
| [TAPAS Base](https://huggingface.co/google/tapas-base) | 1.1, 1.5 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2004.02349), [GitHub](https://github.com/google-research/tapas) |
| [Chronos-T5 Base](https://huggingface.co/amazon/chronos-t5-base) | 1.6 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2403.07815), [GitHub](https://github.com/amazon-science/chronos-forecasting) |
| [FAST+](https://huggingface.co/physical-intelligence/fast) | 1.7 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2501.09747), [GitHub](https://github.com/Physical-Intelligence/openpi) |
| [Sonata](https://huggingface.co/facebook/sonata) | 1.4 | Algorithmic; expert-defined composition | [Paper](https://arxiv.org/abs/2503.16429), [GitHub](https://github.com/facebookresearch/sonata) |
| [TimesFM-2.5-200M](https://huggingface.co/google/timesfm-2.5-200m-pytorch) | 1.6 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2310.10688), [GitHub](https://github.com/google-research/timesfm) |
| [Granite-TimeSeries-TTM-R2](https://huggingface.co/ibm-granite/granite-timeseries-ttm-r2) | 1.6 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2401.03955), [GitHub](https://github.com/ibm-granite/granite-tsfm) |
| [Nucleotide Transformer v2 500M](https://huggingface.co/InstaDeepAI/nucleotide-transformer-v2-500m-multi-species) | 2.1 | Algorithmic; predefined units | [Paper](https://www.nature.com/articles/s41592-024-02523-z), [GitHub](https://github.com/instadeepai/nucleotide-transformer) |
| [DNABERT-2-117M](https://huggingface.co/zhihan1996/DNABERT-2-117M) | 2.1 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2306.15006), [GitHub](https://github.com/MAGICS-LAB/DNABERT_2) |
| [Evo-1.5-8K-base](https://huggingface.co/evo-design/evo-1.5-8k-base) | 2.1 | Algorithmic; predefined units | [Paper](https://www.science.org/doi/10.1126/science.ado9336), [GitHub](https://github.com/evo-design/evo) |
| [RNA-FM](https://huggingface.co/multimolecule/rnafm) | 2.1 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2204.00300), [GitHub](https://github.com/ml4bio/RNA-FM) |
| [Evo 2 40B](https://huggingface.co/arcinstitute/evo2_40b) | 2.1 | Algorithmic; predefined units | [Paper](https://doi.org/10.1038/s41586-026-10176-5), [GitHub](https://github.com/ArcInstitute/evo2) |
| [ESM-2-650M](https://huggingface.co/facebook/esm2_t33_650M_UR50D) | 2.2 | Algorithmic; predefined units | [Paper](https://www.science.org/doi/10.1126/science.ade2574), [GitHub](https://github.com/facebookresearch/esm) |
| [ProtT5-XL-UniRef50](https://huggingface.co/Rostlab/prot_t5_xl_uniref50) | 2.2 | Algorithmic; predefined units | [Paper](https://doi.org/10.1101/2020.07.12.199554), [GitHub](https://github.com/agemagician/ProtTrans) |
| [ESM3-small-open-v1](https://huggingface.co/biohub/esm3-sm-open-v1) | 2.2 | Hybrid; composed tokenizer streams | [Paper](https://www.science.org/doi/10.1126/science.ads0018), [GitHub](https://github.com/Biohub/esm) |
| [PepMLM-650M](https://huggingface.co/ChatterjeeLab/PepMLM-650M) | 2.2 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2310.03842), [GitHub](https://github.com/programmablebio/pepmlm) |
| [ESMC-6B](https://huggingface.co/biohub/esmc-6b-2024-12) | 2.2 | Algorithmic; predefined units | [Paper](https://biohub.ai/papers/esm_protein.pdf), [GitHub](https://github.com/Biohub/esm) |
| [SaProt-650M-AF2](https://huggingface.co/westlake-repl/SaProt_650M_AF2) | 2.2 | Hybrid; composed tokenizer streams | [Paper](https://openreview.net/forum?id=6MRm3G4NiU), [GitHub](https://github.com/westlake-repl/SaProt) |
| [Boltz-2](https://huggingface.co/boltz-community/boltz-2) | 2.1, 2.2, 2.3 | Algorithmic; predefined units | [Paper](https://www.biorxiv.org/content/10.1101/2025.06.14.659707v1.full), [GitHub](https://github.com/jwohlwend/boltz) |
| [Boltz-1](https://huggingface.co/boltz-community/boltz-1) | 2.1, 2.2, 2.3 | Algorithmic; predefined units | [Paper](https://www.biorxiv.org/content/10.1101/2024.11.19.624167v4), [GitHub](https://github.com/jwohlwend/boltz) |
| [Chai-1](https://huggingface.co/chaidiscovery/chai-1) | 2.1, 2.2, 2.3 | Algorithmic; predefined units | [Paper](https://www.biorxiv.org/content/10.1101/2024.10.10.615955v2), [GitHub](https://github.com/chaidiscovery/chai-lab) |
| [Protenix](https://huggingface.co/OneScience-Group/protenix) | 2.1, 2.2, 2.3 | Algorithmic; predefined units | [Paper](https://openreview.net/forum?id=rdupZxS99R), [GitHub](https://github.com/bytedance/Protenix) |
| [MoLFormer-XL-both-10pct](https://huggingface.co/ibm-research/MoLFormer-XL-both-10pct) | 2.3 | Algorithmic; expert-defined composition | [Paper](https://www.nature.com/articles/s42256-022-00580-7), [GitHub](https://github.com/IBM/molformer) |
| [UltraNMR](https://huggingface.co/milesyc/ultranmr) | 2.3, 2.5 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2606.20756), [GitHub](https://github.com/wuycM/UltraNMR) |
| [MatterGen](https://huggingface.co/microsoft/mattergen) | 2.4 | Algorithmic; predefined units | [Paper](https://www.nature.com/articles/s41586-025-08628-5), [GitHub](https://github.com/microsoft/mattergen) |
| [UMA](https://huggingface.co/facebook/UMA) | 2.3, 2.4 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2506.23971), [GitHub](https://github.com/facebookresearch/fairchem) |
| [UNI](https://huggingface.co/MahmoodLab/UNI) | 2.6 | Algorithmic; predefined units | [Paper](https://www.nature.com/articles/s41591-024-02857-3), [GitHub](https://github.com/mahmoodlab/UNI) |
| [MedGemma-1.5-4B-IT](https://huggingface.co/google/medgemma-1.5-4b-it) | 2.6 | Hybrid; composed tokenizer streams | [Paper](https://arxiv.org/abs/2604.05081), [GitHub](https://github.com/Google-Health/medgemma) |
| [Prov-GigaPath](https://huggingface.co/prov-gigapath/prov-gigapath) | 2.6 | Algorithmic; predefined units | [Paper](https://www.nature.com/articles/s41586-024-07441-w), [GitHub](https://github.com/prov-gigapath/prov-gigapath) |
| [Virchow2](https://huggingface.co/paige-ai/Virchow2) | 2.6 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2408.00738) |
| [H-optimus-1](https://huggingface.co/bioptimus/H-optimus-1) | 2.6 | Algorithmic; predefined units | [Paper](https://doi.org/10.1158/1538-7445.AM2026-LB174) |
| [Geneformer](https://huggingface.co/ctheodoris/Geneformer) | 2.7 | Algorithmic; predefined units | [Paper](https://www.nature.com/articles/s41586-023-06139-9) |
| [STATE SE-600M](https://huggingface.co/arcinstitute/SE-600M) | 2.7 | Algorithmic; predefined units | [Paper](https://doi.org/10.1016/j.cell.2026.07.052), [GitHub](https://github.com/ArcInstitute/state) |
| [Stack-Large-Aligned](https://huggingface.co/arcinstitute/Stack-Large-Aligned) | 2.7 | Algorithmic; predefined units | [Paper](https://doi.org/10.64898/2026.01.09.698608), [GitHub](https://github.com/ArcInstitute/stack) |
| [Prithvi-EO-2.0-300M](https://huggingface.co/ibm-nasa-geospatial/Prithvi-EO-2.0-300M) | 2.9 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2412.02732), [GitHub](https://github.com/NASA-IMPACT/Prithvi-EO-2.0) |
| [Aurora](https://huggingface.co/microsoft/aurora) | 2.9 | Algorithmic; predefined units | [Paper](https://www.nature.com/articles/s41586-025-09005-y), [GitHub](https://github.com/microsoft/aurora) |
| [TerraMind-1.0-base](https://huggingface.co/ibm-esa-geospatial/TerraMind-1.0-base) | 2.9 | Hybrid; composed tokenizer streams | [Paper](https://arxiv.org/abs/2504.11171), [GitHub](https://github.com/IBM/terramind) |
| [Prithvi-WxC-1.0-2300M](https://huggingface.co/ibm-nasa-geospatial/Prithvi-WxC-1.0-2300M) | 2.9 | Algorithmic; predefined units | [Paper](https://arxiv.org/abs/2409.13598), [GitHub](https://github.com/NASA-IMPACT/Prithvi-WxC) |
| [TxGemma-2B-predict](https://huggingface.co/google/txgemma-2b-predict) | 2.1, 2.2, 2.3 | Algorithmic; data-learned composition | [Paper](https://arxiv.org/abs/2504.06196), [GitHub](https://github.com/google-gemini/gemma-cookbook/tree/main/TxGemma) |

## Contributing

Corrections and additions are welcome.
