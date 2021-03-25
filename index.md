<html>
   <head></head>
   <body>
      <link rel="stylesheet" type="text/css" href="./github.css" id="_theme">
      <div id="_html" class="markdown-body">
         <meta charset="UTF-8">
         <title>SCD Dataset </title>
         <meta name="description" content="SCD: A Stacked Carton Dataset for Detection and Segmentation">
         <meta name="keywords" content="rpc dataset, rpctool, retail, product detection">
         <link rel="shortcut icon" href="./favicon.ico">
         <div align="center">
            <h1 id="SCD: A Stacked Carton Dataset for Detection and Segmentation">SCD: A Stacked Carton Dataset for Detection and Segmentation</h1>
            <p><strong><a href="https://scholar.google.com/citations?user=8Of_NYQAAAAJ&hl=zh-CN">Jinrong Yang<sup>1</sup></a> &nbsp;&nbsp;&nbsp; <a href="https://scholar.google.com/citations?user=oWHBHDEAAAAJ&hl=zh-CN">Shengkai Wu<sup>1</sup></a> &nbsp;&nbsp;&nbsp; Lijun Gou<sup>1</sup>&nbsp;&nbsp;&nbsp; Hangcheng Yu<sup>1</sup> &nbsp;&nbsp;&nbsp; Chenxi Lin<sup>1</sup> &nbsp;&nbsp;&nbsp; Jiazhuo Wang<sup>1</sup> &nbsp;&nbsp;&nbsp; Minxuan Li<sup>2</sup> &nbsp;&nbsp;&nbsp; Xiaoping Li<sup>1</sup></strong></p>
            <p><sup>1</sup>State Key Laboratory of Digital Manufacturing Equipment and Technology, Huazhong University of Science and Technology, China.<br><sup>2</sup>Faculty of Arts and Science, Queen’s University, Canada</p>
            <hr>
            <h3 id="abstract--paper--dataset--baselines--leaderboard--rpc-tool"><a href="#1-abstract">Abstract</a> | <a href="#2-paper">Paper</a> | <a href="#3-our-rpc-dataset">Dataset</a> | <a href="#4-proposed-baseline-method-on-the-rpc-dataset">Baselines</a> | <a href="#5-Leaderboard">Leaderboard</a> | <a href="#6-rpc-tool">RPC-tool</a></h3>
         </div>
         <h2 id="1-abstract"><a class="anchor" name="1-abstract" href="#1-abstract"><span class="octicon octicon-link"></span></a>1. Abstract</h2>
         <p style="text-align: justify"><em>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Carton detection is an important technique in the automatic logistics system and can be applied to many applications such as the stacking and unstacking of cartons, the unloading of cartons in the containers. However, there is no public large-scale carton dataset for the research community to train and evaluate the carton detection models up to now, which hinders the development of carton detection. In this paper, we present a large-scale carton dataset named Stacked Carton Dataset(SCD) with the goal of advancing the state-of-the-art in carton detection. Images are collected from the internet and several warehourses, and objects are labeled using per-instance segmentation for precise localization. There are totally 250,000 instance masks from 16,136 images. In addition, we design a carton detector based on RetinaNet by embedding Boundary Guided Supervision module(BGS) and Offset Prediction between Classification and Localization module(OPCL). OPCL alleviates the imbalance problem between classification and localization quality which boosts AP by 3.1% ~ 4.7% on SCD while BGS guides the detector to pay more attention to boundary information of cartons and decouple repeated carton textures. To demonstrate the generalization of OPCL to other datasets, we conduct extensive experiments on MS COCO and PASCAL VOC. The improvements of AP on MS COCO and PASCAL VOC are 1.8% ~ 2.2% and 3.4% ~ 4.3% respectively.</em></p>
         <h2 id="2-paper"><a class="anchor" name="2-paper" href="#2-paper"><span class="octicon octicon-link"></span></a>2. Paper</h2>
         <div align="center">
            <a href="https://https://arxiv.org/abs/2102.12808">
            <img style="width:200px" src="imgs/paper_small.jpg">
            </a>   
            <p><a href="https://arxiv.org/abs/2102.12808"><strong>Paper on arXiv =&gt; "SCD: A Stacked Carton Dataset for Detection and Segmentation"</strong></a></p>
         </div>
         <h2 id="3-SCD"><a class="anchor" name="3-SCD" href="#3-SCD"><span class="octicon octicon-link"></span></a>3. SCD</h2>
         <div align="center">
            <p><a href="https://www.kaggle.com/diyer22/retail-product-checkout-dataset"><img src="imgs/rpc-dataset.png" alt=""></a>     </p>
            <p><a href="https://pan.baidu.com/s/1p2KOYFhLWFfbmMBLpxbVMA"><strong>OSCD =&gt; "OSCD: Images and COCO-style labels"</strong></a>
               (password: 0000)
            </p>
            <p><a href="https://pan.baidu.com/s/1dmk6mFPEKckkiaNg9qdN3g"><strong>LSCD =&gt; "OSCD: Images and LabelMe-style labels"</strong></a>
               (password: 0000)
            </p>
            <p><a href="https://pan.baidu.com/s/1J3e1PIWsf0LBnyWu9OmUsQ"><strong>LSCD =&gt; "OSCD: Images and COCO-style labels(containing Carton-inner-all, Carton-inner-occlusion, Carton-outer-all and Carton-outer-occlusion)"</strong></a>
               (password: 0000)
            </p>
            <p><a href="https://pan.baidu.com/s/1WV_5yxIiPWhs6L2gszzekg"><strong>LSCD =&gt; "OSCD: Images and COCO-style labels(only containing carton)"</strong></a>
               (password: 0000)
            </p>
         </div>
         <p>*<strong>Notice</strong>: If downloading from Kaggle is not accessable, you can alternatively download the dataset using <a href="https://pan.baidu.com/s/1vrrLaSpJe5JxT3zhYfOaog">Baidu Drive</a>.</p>
         <h4 id="31-dataset-license"><a class="anchor" name="31-dataset-license" href="#31-dataset-license"><span class="octicon octicon-link"></span></a>3.1 Dataset license:</h4>
         <p><a href="https://creativecommons.org/licenses/by-nc-sa/4.0/"><img src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png" alt=""></a><br>CC BY-NC-SA 4.0</p>
         <h4 id="32-overview-infomation-of-the-rpc-dataset"><a class="anchor" name="32-overview-infomation-of-the-rpc-dataset" href="#32-overview-infomation-of-the-rpc-dataset"><span class="octicon octicon-link"></span></a>3.2 Overview infomation of the RPC dataset</h4>
         <div align="center">
            <table>
               <thead>
                  <tr>
                     <th><em>Split</em></th>
                     <th align="right"><em># images</em></th>
                     <th align="right"><em># objects</em></th>
                     <th align="right"><em># objects/image</em></th>
                     <th align="right"><em># categories/image</em></th>
                  </tr>
               </thead>
               <tbody>
                  <tr>
                     <td>Training set (Exemplar images)</td>
                     <td align="right">53,739</td>
                     <td align="right">53,739</td>
                     <td align="right">1</td>
                     <td align="right">1</td>
                  </tr>
                  <tr>
                     <td>Validation set (Checkout images)</td>
                     <td align="right">6,000</td>
                     <td align="right">73,602</td>
                     <td align="right">12.27</td>
                     <td align="right">6.33</td>
                  </tr>
                  <tr>
                     <td>Test set (Checkout images)</td>
                     <td align="right">24,000</td>
                     <td align="right">294,333</td>
                     <td align="right">12.26</td>
                     <td align="right">6.31</td>
                  </tr>
               </tbody>
            </table>
         </div>
         <h4 id="33-collection-equipment-for-single-product-images-training-set"><a class="anchor" name="33-collection-equipment-for-single-product-images-training-set" href="#33-collection-equipment-for-single-product-images-training-set"><span class="octicon octicon-link"></span></a>3.3 Collection equipment for single product images (training set)</h4>
         <div align="center">
            <a href="https://www.kaggle.com/diyer22/retail-product-checkout-dataset#retail_product_checkout.zip">
            <img style="width:700px" src="imgs/single.png">
            </a>   
         </div>
         <h4 id="34-different-clutter-levels-for-checkout-images-valtest-sets"><a class="anchor" name="34-different-clutter-levels-for-checkout-images-valtest-sets" href="#34-different-clutter-levels-for-checkout-images-valtest-sets"><span class="octicon octicon-link"></span></a>3.4 Different clutter levels for checkout images (val/test sets)</h4>
         <div align="center">
            <a href="https://www.kaggle.com/diyer22/retail-product-checkout-dataset#retail_product_checkout.zip">
            <img style="width:500px" src="imgs/test.png">
            </a>   
         </div>
         <h4 id="35-detailed-information-of-valtest-sets-for-different-clutters"><a class="anchor" name="35-detailed-information-of-valtest-sets-for-different-clutters" href="#35-detailed-information-of-valtest-sets-for-different-clutters"><span class="octicon octicon-link"></span></a>3.5 Detailed information of val+test sets for different clutters</h4>
         <div align="center">
            <table>
               <thead>
                  <tr>
                     <th><em>Clutter mode</em></th>
                     <th align="right"><em># images</em></th>
                     <th align="right"><em># objects</em></th>
                     <th align="right"><em># objects/image</em></th>
                     <th align="right"><em># categories/image</em></th>
                  </tr>
               </thead>
               <tbody>
                  <tr>
                     <td>Easy</td>
                     <td align="right">10,000</td>
                     <td align="right">71,496</td>
                     <td align="right">7.15</td>
                     <td align="right">3.81</td>
                  </tr>
                  <tr>
                     <td>Medium</td>
                     <td align="right">10,000</td>
                     <td align="right">122,961</td>
                     <td align="right">12.30</td>
                     <td align="right">6.27</td>
                  </tr>
                  <tr>
                     <td>Hard</td>
                     <td align="right">10,000</td>
                     <td align="right">173,478</td>
                     <td align="right">17.35</td>
                     <td align="right">8.87</td>
                  </tr>
               </tbody>
            </table>
         </div>
         <h2 id="4-proposed-baseline-method-on-the-rpc-dataset"><a class="anchor" name="4-proposed-baseline-method-on-the-rpc-dataset" href="#4-proposed-baseline-method-on-the-rpc-dataset"><span class="octicon octicon-link"></span></a>4. Proposed baseline method on the RPC dataset</h2>
         <h4 id="41-pipeline-of-our-synrender-method"><a class="anchor" name="41-pipeline-of-our-synrender-method" href="#41-pipeline-of-our-synrender-method"><span class="octicon octicon-link"></span></a>4.1 Pipeline of our <em>Syn+Render</em> method</h4>
         <div align="center">
            <img style="width:700px" src="imgs/pipeline.png">
         </div>
         <h4 id="42-experimental-results"><a class="anchor" name="42-experimental-results" href="#42-experimental-results"><span class="octicon octicon-link"></span></a>4.2 Experimental results</h4>
         <div align="center">
            <img style="width:700px" src="imgs/result.png">
         </div>
         <h2 id="5-leaderboard"><a class="anchor" name="5-leaderboard" href="#5-leaderboard"><span class="octicon octicon-link"></span></a>5. Leaderboard</h2>
         <div style="text-align: justify">
            <p><a href="https://github.com/RPC-Dataset/RPC-Leaderboard"><strong>RPC-Leaderboard</strong></a></p>
            <p>If you have been successful in creating a model based on the training set and it performs well on the validation set, we encourage you to run your model on the test set. The  <a href="https://github.com/DIYer22/retail_product_checkout_tools"><code>rpctool</code></a> (in the next section in this project page) will contribute to return the corresponding results of the evaluation metrics. You can submit your results on the RPC leaderboard by creating a new issue. Your results will be ranked in the leaderboard and to benchmark your approach against that of other machine learners. We are looking forward to your submission. Please click <a href="https://github.com/RPC-Dataset/RPC-Leaderboard/issues">here</a> to submit.</p>
         </div>
         <h2 id="6-rpc-tool"><a class="anchor" name="6-rpc-tool" href="#6-rpc-tool"><span class="octicon octicon-link"></span></a>6. RPC-tool</h2>
         <div style="text-align: justify">
            <p><a href="https://github.com/DIYer22/retail_product_checkout_tools"><code>rpctool</code></a>: A Python package for evaluating your methods on the RPC dataset. It can return several evaluation metrics (listed in the aforementioned table in Sec. 4.2). More information can be found in <a href="https://github.com/DIYer22/retail_product_checkout_tools"><code>rpctool</code></a>.</p>
         </div>
         <h2 id="7-attn"><a class="anchor" name="7-attn" href="#7-attn"><span class="octicon octicon-link"></span></a>7. ATTN</h2>
         <div style="text-align: justify">
            <p>This dataset and code packages are free for academic usage. You can run them at your own risk. For other purposes, please contact the corresponding author Dr. Xiu-Shen Wei (weixs.gm [at] gmail.com).</p>
         </div>
         <!-- Global site tag (gtag.js) - Google Analytics -->
         <script async="" src="https://www.googletagmanager.com/gtag/js?id=UA-133191784-1"></script>
         <script>
            window.dataLayer = window.dataLayer || [];
            function gtag(){dataLayer.push(arguments);}
            gtag('js', new Date());
            
            gtag('config', 'UA-133191784-1');
         </script>
      </div>
   </body>
</html>