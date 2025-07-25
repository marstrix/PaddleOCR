# Introduction to PP-StructureV3

**PP-StructureV3** pipeline, based on the Layout Parsing v1 pipeline, has strengthened the ability of layout detection, table recognition, and formula recognition. It has also added the ability to understand charts and restore reading order, as well as the ability to convert results into Markdown files. In various document data, it performs excellently and can handle more complex document data. This pipeline also provides flexible service-oriented deployment methods, supporting the use of multiple programming languages on various hardware. Moreover, it also provides the ability for secondary development. You can train and optimize on your own dataset based on this pipeline, and the trained model can be seamlessly integrated.

<div align="center">
<img src="https://raw.githubusercontent.com/cuicheng01/PaddleX_doc_images/refs/heads/main/images/paddleocr/PP-StructureV3/algorithm_ppstructurev3.png" width="600"/>
</div>

# Key Metrics
<table>
  <thead>
    <tr>
      <th rowspan="2">Method Type</th>
      <th rowspan="2">Methods</th>
      <th colspan="2">Overall<sup>Edit</sup>↓</th>
      <th colspan="2">Text<sup>Edit</sup>↓</th>
      <th colspan="2">Formula<sup>Edit</sup>↓</th>
      <th colspan="2">Table<sup>Edit</sup>↓</th>
      <th colspan="2">Read Order<sup>Edit</sup>↓</th>
    </tr>
    <tr>
      <th>EN</th>
      <th>ZH</th>
      <th>EN</th>
      <th>ZH</th>
      <th>EN</th>
      <th>ZH</th>
      <th>EN</th>
      <th>ZH</th>
      <th>EN</th>
      <th>ZH</th>
    </tr>
  </thead>
 <tbody>
  <tr> 
   <td rowspan="9">Pipeline Tools</td> 
   <td><b>PP-structureV3</b></td> 
   <td><b>0.145</b></td> 
   <td><b>0.206</b></td> 
   <td>0.058</td> 
   <td><b>0.088</b></td> 
   <td>0.295</td> 
   <td>0.535</td> 
   <td>0.159</td> 
   <td><b>0.109</b></td> 
   <td>0.069</td> 
   <td><b>0.091</b></td> 
  </tr> 
  <tr> 
   <td>MinerU-0.9.3</td> 
   <td>0.15</td> 
   <td>0.357</td> 
   <td>0.061</td> 
   <td>0.215</td> 
   <td>0.278</td> 
   <td>0.577</td> 
   <td>0.18</td> 
   <td>0.344</td> 
   <td>0.079</td> 
   <td>0.292</td> 
  </tr> 
  <tr> 
   <td>MinerU-1.3.11</td> 
   <td>0.166</td> 
   <td>0.310</td> 
   <td>0.0826</td> 
   <td>0.2000</td> 
   <td>0.3368</td> 
   <td>0.6236</td> 
   <td>0.1613</td> 
   <td>0.1833</td> 
   <td>0.0834</td> 
   <td>0.2316</td> 
  </tr> 
  <tr> 
   <td>Marker-1.2.3</td> 
   <td>0.336</td> 
   <td>0.556</td> 
   <td>0.08</td> 
   <td>0.315</td> 
   <td>0.53</td> 
   <td>0.883</td> 
   <td>0.619</td> 
   <td>0.685</td> 
   <td>0.114</td> 
   <td>0.34</td> 
  </tr> 
  <tr> 
   <td>Mathpix</td> 
   <td>0.191</td> 
   <td>0.365</td> 
   <td>0.105</td> 
   <td>0.384</td> 
   <td>0.306</td> 
   <td>0.454</td> 
   <td>0.243</td> 
   <td>0.32</td> 
   <td>0.108</td> 
   <td>0.304</td> 
  </tr> 
  <tr> 
   <td>Docling-2.14.0</td> 
   <td>0.589</td> 
   <td>0.909</td> 
   <td>0.416</td> 
   <td>0.987</td> 
   <td>0.999</td> 
   <td>1</td> 
   <td>0.627</td> 
   <td>0.81</td> 
   <td>0.313</td> 
   <td>0.837</td> 
  </tr> 
  <tr> 
   <td>Pix2Text-1.1.2.3</td> 
   <td>0.32</td> 
   <td>0.528</td> 
   <td>0.138</td> 
   <td>0.356</td> 
   <td><b>0.276</b></td> 
   <td>0.611</td> 
   <td>0.584</td> 
   <td>0.645</td> 
   <td>0.281</td> 
   <td>0.499</td> 
  </tr> 
  <tr> 
   <td>Unstructured-0.17.2</td> 
   <td>0.586</td> 
   <td>0.716</td> 
   <td>0.198</td> 
   <td>0.481</td> 
   <td>0.999</td> 
   <td>1</td> 
   <td>1</td> 
   <td>0.998</td> 
   <td>0.145</td> 
   <td>0.387</td> 
  </tr> 
  <tr> 
   <td>OpenParse-0.7.0</td> 
   <td>0.646</td> 
   <td>0.814</td> 
   <td>0.681</td> 
   <td>0.974</td> 
   <td>0.996</td> 
   <td>1</td> 
   <td>0.284</td> 
   <td>0.639</td> 
   <td>0.595</td> 
   <td>0.641</td> 
  </tr> 
  <tr> 
   <td rowspan="5">Expert VLMs</td> 
   <td>GOT-OCR</td> 
   <td>0.287</td> 
   <td>0.411</td> 
   <td>0.189</td> 
   <td>0.315</td> 
   <td>0.36</td> 
   <td>0.528</td> 
   <td>0.459</td> 
   <td>0.52</td> 
   <td>0.141</td> 
   <td>0.28</td> 
  </tr> 
  <tr> 
   <td>Nougat</td> 
   <td>0.452</td> 
   <td>0.973</td> 
   <td>0.365</td> 
   <td>0.998</td> 
   <td>0.488</td> 
   <td>0.941</td> 
   <td>0.572</td> 
   <td>1</td> 
   <td>0.382</td> 
   <td>0.954</td> 
  </tr> 
  <tr> 
   <td>Mistral OCR</td> 
   <td>0.268</td> 
   <td>0.439</td> 
   <td>0.072</td> 
   <td>0.325</td> 
   <td>0.318</td> 
   <td>0.495</td> 
   <td>0.6</td> 
   <td>0.65</td> 
   <td>0.083</td> 
   <td>0.284</td> 
  </tr> 
  <tr> 
   <td>OLMOCR-sglang</td> 
   <td>0.326</td> 
   <td>0.469</td> 
   <td>0.097</td> 
   <td>0.293</td> 
   <td>0.455</td> 
   <td>0.655</td> 
   <td>0.608</td> 
   <td>0.652</td> 
   <td>0.145</td> 
   <td>0.277</td> 
  </tr> 
  <tr> 
   <td>SmolDocling-256M_transformer</td> 
   <td>0.493</td> 
   <td>0.816</td> 
   <td>0.262</td> 
   <td>0.838</td> 
   <td>0.753</td> 
   <td>0.997</td> 
   <td>0.729</td> 
   <td>0.907</td> 
   <td>0.227</td> 
   <td>0.522</td> 
  </tr> 
  <tr> 
   <td rowspan="6">General VLMs</td> 
   <td>Gemini2.0-flash</td> 
   <td>0.191</td> 
   <td>0.264</td> 
   <td>0.091</td> 
   <td>0.139</td> 
   <td>0.389</td> 
   <td>0.584</td> 
   <td>0.193</td> 
   <td>0.206</td> 
   <td>0.092</td> 
   <td>0.128</td> 
  </tr> 
  <tr> 
   <td>Gemini2.5-Pro</td> 
   <td>0.148</td> 
   <td><b>0.212</b></td> 
   <td><b>0.055</b></td> 
   <td>0.168</td> 
   <td>0.356</td> 
   <td>0.439</td> 
   <td><b>0.13</b></td> 
   <td>0.119</td> 
   <td><b>0.049</b></td> 
   <td>0.121</td> 
  </tr> 
  <tr> 
   <td>GPT4o</td> 
   <td>0.233</td> 
   <td>0.399</td> 
   <td>0.144</td> 
   <td>0.409</td> 
   <td>0.425</td> 
   <td>0.606</td> 
   <td>0.234</td> 
   <td>0.329</td> 
   <td>0.128</td> 
   <td>0.251</td> 
  </tr> 
  <tr> 
   <td>Qwen2-VL-72B</td> 
   <td>0.252</td> 
   <td>0.327</td> 
   <td>0.096</td> 
   <td>0.218</td> 
   <td>0.404</td> 
   <td>0.487</td> 
   <td>0.387</td> 
   <td>0.408</td> 
   <td>0.119</td> 
   <td>0.193</td> 
  </tr> 
  <tr> 
   <td>Qwen2.5-VL-72B</td> 
   <td>0.214</td> 
   <td>0.261</td> 
   <td>0.092</td> 
   <td>0.18</td> 
   <td>0.315</td> 
   <td><b>0.434</b></td> 
   <td>0.341</td> 
   <td>0.262</td> 
   <td>0.106</td> 
   <td>0.168</td> 
  </tr> 
  <tr> 
   <td>InternVL2-76B</td> 
   <td>0.44</td> 
   <td>0.443</td> 
   <td>0.353</td> 
   <td>0.29</td> 
   <td>0.543</td> 
   <td>0.701</td> 
   <td>0.547</td> 
   <td>0.555</td> 
   <td>0.317</td> 
   <td>0.228</td> 
  </tr> 
 </tbody>
</table>

The above data is from:
* <a href="https://github.com/opendatalab/OmniDocBench">OmniDocBench</a>
* <a href="https://arxiv.org/abs/2412.07626">OmniDocBench: Benchmarking Diverse PDF Document Parsing with Comprehensive Annotations</a>

# End to End Benchmark

The performance of PP-StructureV3 and MinerU with different configurations under different GPU environments are as follows.

Requirements:
* Paddle 3.0
* PaddleOCR 3.0.0
* MinerU 1.3.10
* CUDA 11.8
* cuDNN 8.9

## Local inference

Local inference was tested with both V100 and A100 GPU, evaluating the performance of PP-StructureV3 under 6 different configurations. The test data consists of 15 PDF files, totaling 925 pages, including elements such as tables, formulas, seals, and charts.

In the following PP-StructureV3 configuration, please refer to [PP-OCRv5](../PP-OCRv5/PP-OCRv5.en.md) for OCR model details, see [Formula Recognition](../../module_usage/formula_recognition.en.md) for formula recognition model details, and refer to [Text Detection](../../module_usage/text_detection.en.md) for the max_side_limit setting of the text detection module.

### Env: NVIDIA Tesla V100 + Intel Xeon Gold 6271C

<table border="1">
 <tr>
  <td>
   Methods
  </td>
  <td colspan="4">
   Configurations
  </td>
  <td rowspan="2">
   Average time per
  page
    (s)
  </td>
  <td rowspan="2">
   Average CPU
    （%）
  </td>
  <td rowspan="2">
   Peak RAM Usage
    （GB）
  </td>
  <td rowspan="2">
   Average RAM
  Usage
    （GB）
  </td>
  <td rowspan="2">
   Average GPU
    （%）
  </td>
  <td rowspan="2">
   Peak VRAM Usage
    （GB）
  </td>
  <td rowspan="2">
   Average VRAM
  Usage
    （GB）
  </td>
 </tr>
 <tr>
  <td rowspan="7">
   PP-StructureV3
  </td>
  <td>
   OCR Models
  </td>
  <td>
   Formula Recognition Model
  </td>
  <td>
   Chart Recognition Model
  </td>
  <td>
   text detection module max_side_limit
  </td>
 </tr>
 <tr>
  <td>
   Server
  </td>
  <td>
   PP-FormulaNet-L
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   1.77
  </td>
  <td>
   111.4
  </td>
  <td>
   6.7
  </td>
  <td>
   5.2
  </td>
  <td>
   38.9
  </td>
  <td>
   17.0
  </td>
  <td>
   16.5
  </td>
 </tr>
 <tr>
  <td>
   Server
  </td>
  <td>
   PP-FormulaNet-L
  </td>
  <td>
   ✔
  </td>
  <td>
   4096
  </td>
  <td>
   4.09
  </td>
  <td>
   105.3
  </td>
  <td>
   5.5
  </td>
  <td>
   4.0
  </td>
  <td>
   24.7
  </td>
  <td>
   17.0
  </td>
  <td>
   16.6
  </td>
 </tr>
 <tr>
  <td>
   Mobile
  </td>
  <td>
   PP-FormulaNet-L
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   1.56
  </td>
  <td>
   113.7
  </td>
  <td>
   6.6
  </td>
  <td>
   4.9
  </td>
  <td>
   29.1
  </td>
  <td>
   10.7
  </td>
  <td>
   10.6
  </td>
 </tr>
 <tr>
  <td>
   Server
  </td>
  <td>
   PP-FormulaNet-M
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   1.42
  </td>
  <td>
   112.9
  </td>
  <td>
   6.8
  </td>
  <td>
   5.1
  </td>
  <td>
   38
  </td>
  <td>
   16.0
  </td>
  <td>
   15.5
  </td>
 </tr>
 <tr>
  <td>
   Mobile
  </td>
  <td>
   PP-FormulaNet-M
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   1.15
  </td>
  <td>
   114.8
  </td>
  <td>
   6.5
  </td>
  <td>
   5.0
  </td>
  <td>
   26.1
  </td>
  <td>
   8.4
  </td>
  <td>
   8.3
  </td>
 </tr>
 <tr>
  <td>
   Mobile
  </td>
  <td>
   PP-FormulaNet-M
  </td>
  <td>
   ✗
  </td>
  <td>
   1200
  </td>
  <td>
   0.99
  </td>
  <td>
   113
  </td>
  <td>
   7.0
  </td>
  <td>
   5.6
  </td>
  <td>
   29.2
  </td>
  <td>
   8.6
  </td>
  <td>
   8.5
  </td>
 </tr>
 <tr>
  <td>
   MinerU
  </td>
  <td colspan="4">
   -
  </td>
  <td>
   1.57
  </td>
  <td>
   142.9
  </td>
  <td>
   13.3
  </td>
  <td>
   11.8
  </td>
  <td>
   43.3
  </td>
  <td>
   31.6
  </td>
  <td>
   9.7
  </td>
 </tr>
</table>

### NVIDIA A100 + Intel Xeon Platinum 8350C

<table border="1">
 <tr>
  <td>
   Methods
  </td>
  <td colspan="4">
   Configurations
  </td>
  <td rowspan="2">
   Average time per
  page
    (s)
  </td>
  <td rowspan="2">
   Average CPU
    （%）
  </td>
  <td rowspan="2">
   Peak RAM Usage
    （GB）
  </td>
  <td rowspan="2">
   Average RAM
  Usage
    （GB）
  </td>
  <td rowspan="2">
   Average GPU
    （%）
  </td>
  <td rowspan="2">
   Peak VRAM Usage
    （GB）
  </td>
  <td rowspan="2">
   Average VRAM
  Usage
    （GB）
  </td>
 </tr>
 <tr>
  <td rowspan="7">
   PP-StructureV3
  </td>
  <td>
   OCR Models
  </td>
  <td>
   Formula Recognition Model
  </td>
  <td>
   Chart Recognition Model
  </td>
  <td>
   text detection module max_side_limit
  </td>
 </tr>
 <tr>
  <td>
   Server
  </td>
  <td>
   PP-FormulaNet-L
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   1.12
  </td>
  <td>
   109.8
  </td>
  <td>
   9.2
  </td>
  <td>
   7.8
  </td>
  <td>
   29.8
  </td>
  <td>
   21.8
  </td>
  <td>
   21.1
  </td>
 </tr>
 <tr>
  <td>
   Server
  </td>
  <td>
   PP-FormulaNet-L
  </td>
  <td>
   ✔
  </td>
  <td>
   4096
  </td>
  <td>
   2.76
  </td>
  <td>
   103.7
  </td>
  <td>
   9.0
  </td>
  <td>
   7.7
  </td>
  <td>
   24
  </td>
  <td>
   21.8
  </td>
  <td>
   21.1
  </td>
 </tr>
 <tr>
  <td>
   Mobile
  </td>
  <td>
   PP-FormulaNet-L
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   1.04
  </td>
  <td>
   110.7
  </td>
  <td>
   9.3
  </td>
  <td>
   7.8
  </td>
  <td>
   22
  </td>
  <td>
   12.2
  </td>
  <td>
   12.1
  </td>
 </tr>
 <tr>
  <td>
   Server
  </td>
  <td>
   PP-FormulaNet-M
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   0.95
  </td>
  <td>
   111.4
  </td>
  <td>
   9.1
  </td>
  <td>
   7.8
  </td>
  <td>
   28.1
  </td>
  <td>
   21.8
  </td>
  <td>
   21.0
  </td>
 </tr>
 <tr>
  <td>
   Mobile
  </td>
  <td>
   PP-FormulaNet-M
  </td>
  <td>
   ✗
  </td>
  <td>
   4096
  </td>
  <td>
   0.89
  </td>
  <td>
   112.1
  </td>
  <td>
   9.2
  </td>
  <td>
   7.8
  </td>
  <td>
   18.5
  </td>
  <td>
   11.4
  </td>
  <td>
   11.2
  </td>
 </tr>
 <tr>
  <td>
   Mobile
  </td>
  <td>
   PP-FormulaNet-M
  </td>
  <td>
   ✗
  </td>
  <td>
   1200
  </td>
  <td>
   0.64
  </td>
  <td>
   113.5
  </td>
  <td>
   10.2
  </td>
  <td>
   8.5
  </td>
  <td>
   23.7
  </td>
  <td>
   11.4
  </td>
  <td>
   11.2
  </td>
 </tr>
 <tr>
  <td>
   MinerU
  </td>
  <td colspan="4">
   -
  </td>
  <td>
   1.06
  </td>
  <td>
   168.3
  </td>
  <td>
   18.3
  </td>
  <td>
   16.8
  </td>
  <td>
   27.5
  </td>
  <td>
   76.9
  </td>
  <td>
   14.8
  </td>
 </tr>
</table>

## Serving Inference

The serving inference test is based on the NVIDIA A100 + Intel Xeon Platinum 8350C environment, with test data consisting of 1500 images, including tables, formulas, seals, charts, and other elements.

<table>
 <tbody>
  <tr> 
   <td>Instances Number</td> 
   <td>Concurrent Requests Number</td> 
   <td>Throughput</td> 
   <td>Average Latency (s)</td> 
   <td>Success Number/Total Number</td> 
  </tr> 
  <tr"> 
   <td>4 GPUs ✖️ 1 instance/gpu</td> 
   <td>4</td> 
   <td>1.69</td> 
   <td>2.36</td> 
   <td>100%</td> 
  </tr> 
  <tr"> 
   <td>4 GPUs ✖️ 4 instances/gpu</td> 
   <td>16</td> 
   <td>4.05</td> 
   <td>3.87</td> 
   <td>100%</td> 
  </tr> 
 </tbody>
</table>

# PP-StructureV3 Demo

<div align="center">
<img src="https://raw.githubusercontent.com/cuicheng01/PaddleX_doc_images/refs/heads/main/images/paddleocr/PP-StructureV3/algorithm_ppstructurev3_demo.png" width="600"/>
</div>

<a href="https://paddle-model-ecology.bj.bcebos.com/paddlex%2FPaddleX3.0%2Fdoc_images%2FPP-StructureV3%2Falgorithm_ppstructurev3_demo.pdf">More Demos</a>


# FAQ

1. What is the default configuration? How to get higher accuracy, faster speed, or smaller GPU memory?

When using mobile OCR models + PP-FormulaNet_plus-M, and max length of text detection set to 1200, if set use_chart_recognition to False and dont not load the chart recognition model, the GPU memory would be reduced. 

On the V100, the peak and average GPU memory would be reduced from 8776.0 MB and 8680.8 MB to 6118.0 MB and 6016.7 MB, respectively; On the A100, the peak and average GPU memory would be reduced from 11716.0 MB and 11453.9 MB to 9850.0 MB and 9593.5 MB, respectively.

You can using multi-gpus by setting `device` to `gpu:<no.>,<no.>`, such as `gpu:0,1,2,3`. And about multi-process parallel inference, you can refer: [Multi-Process Parallel Inference](https://github.com/PaddlePaddle/PaddleX/blob/develop/docs/pipeline_usage/instructions/parallel_inference.en.md#example-of-multi-process-parallel-inference).

2. About serving deployment

(1) Can the service handle requests concurrently?

For the basic serving deployment solution, the service processes only one request at a time. This plan is mainly used for rapid verification, to establish the development chain, or for scenarios where concurrent requests are not required.

For high-stability serving deployment solution, the service process only one request at a time by default, but you can refer to the related docs to adjust achieve scaling.

（2）How to reduce latency and improve throughput?

Use the High-performance inference plugin, and deploy multi instances.
