---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

`CDEHP Dataset` is a large scale multimodal event-based human pose dataset. If you are interesting about building multimodal dataset, please refer to [How to Make](/how-to-make).

## Introduction

We are proud to announce a new large scale multimodal event-based dataset `CDEHP Dataset`(**C**olor **D**epth **E**vent **H**uman **P**ose). `CDEHP Dataset` uses RGB, Depth, and Event cameras to capture actions, bringing a new benchmark to the research of multi-modal models. Of course, you can also use this dataset to carry out research work in the RGB-D field or event camera field.

### Action Class

#### Indoor Actions (13)

| ID    | Action Name   | ID    | Action Name       | ID    | Action Name          | ID    | Action Name              |
| :---: | :-----------: | :---: | :---------------: | :---: | :------------------: | :---: | :----------------------: |
| A1    | walking       | A2    | squat jumping     | A3    | boxing               | A4    | picking up               |
| A5    | jumping jack  | A6    | crotch high five  | A7    | sweeping             | A8    | alternate jumping lunge  |
| A9    | big jump      | A10   | sit-up jump       | A11   | shuttlecock kicking  | A12   | throwing                 |
| A13   | spinning      |       |                   |       |                      |       |                          |

#### Outdoor Actions (25)

|   ID   |   Action Name      |   ID   |   Action Name   |   ID   |   Action Name             |   ID   |   Action Name             |
| :----: | :----------------: | :----: | :-------------: | :----: | :-----------------------: | :----: | :-----------------------: |
|   A15  |   running          |   A16  |   squat jumping |   A17  |   frog jump               |   A18  |   jump fwd/bwd/left/right |
|   A19  |   boxing           |   A20  |   picking up    |   A21  |   cartwheel               |   A22  |   jumping jack            |
|   A23  |   crotch high five |   A24  |   crawling      |   A25  |   rope skipping           |   A26  |   sweeping                |
|   A27  |   mopping          |   A28  |   cycling       |   A29  |   alternate jumping lunge |   A30  |   big jump                |
|   A31  |   sit-up jump      |   A32  |   kicking       |   A33  |   jump shot               |   A34  |   shuttlecock kicking     |
|   A35  |   spinning         |   A36  |   throwing      |   A37  |   long jump               |   A38  |   burpee                  |


### Action Samples

![Indoonsamples of all action classes](/assets/Indoor.png)
![Outdoor samples of all action classes](/assets/Outdoor.png)

## Citation

To cite our datasets, please refer to:

```text
@article{Zhanpeng Shao:2024,
   TITLE      = {A temporal densely connected recurrent network for event-based human pose estimation},
   JOURNAL    = {Pattern Recognition},
   VOLUME     = {147},
   PAGES      = {110048},
   YEAR       = {2024},
   ISSN       = {0031-3203},
   DOI        = {https://doi.org/10.1016/j.patcog.2023.110048},
   URL        = {https://www.sciencedirect.com/science/article/pii/S0031320323007458},
   AUTHOR     = {Zhanpeng Shao and Xueping Wang and Wen Zhou and Wuzhen Wang and Jianyu Yang and Youfu Li},
   KEYWORDS   = {Event signal, Human pose estimation, Dense connections, Recurrent network, Dataset},
   ABSTRACT   = {Event camera is an emerging bio-inspired vision sensors that report per-pixel brightness changes asynchronously. It holds noticeable advantage of high dynamic range, high speed response, and low power budget that enable it to best capture local motions in uncontrolled environments. This motivates us to unlock the potential of event cameras for human pose estimation, as the human pose estimation with event cameras is rarely explored. Due to the novel paradigm shift from conventional frame-based cameras, however, event signals in a time interval contain very limited information, as event cameras can only capture the moving body parts and ignores those static body parts, resulting in some parts to be incomplete or even disappeared in the time interval. This paper proposes a novel densely connected recurrent architecture to address the problem of incomplete information. By this recurrent architecture, we can explicitly model not only the sequential but also non-sequential geometric consistency across time steps to accumulate information from previous frames to recover the entire human bodies, achieving a stable and accurate human pose estimation from event data. Moreover, to better evaluate our model, we collect a large-scale multimodal event-based dataset that comes with human pose annotations, which is by far the most challenging one to the best of our knowledge. The experimental results on two public datasets and our own dataset demonstrate the effectiveness and strength of our approach. Code is available online for facilitating the future research.}
}
```

## Use Dataset

* The size of the `CDEHP Dataset` is large, but we have prepared a variety of official distribution channels. Please follow the [download page](/download) to download the dataset and annotation files, please remember to verify the size of each fragment.
* In order to make subsequent research results comparable, `CDEHP Dataset` officially divides the verification set. **Please follow this method to ensure the fairness of the research work.**

## Projects

* [Website](https://github.com/CDEHP-Dataset/cdehp-dataset.github.io): This website, for promotion, distribution and feedback.
* [PyCeleX5](https://github.com/CDEHP-Dataset/PyCeleX5): CelePixel CeleX5-MIPI C++ API Wrapper for Python 3.
* [Calibration-Tool](https://github.com/CDEHP-Dataset/Calibration-Tool): Twin calibration tools for RGB cameras and event cameras.
* [Recording-Tool](https://github.com/CDEHP-Dataset/Calibration-Tool): Recording tools for making CDEHP-Dataset.
* [Annotation-Tool](https://github.com/CDEHP-Dataset/Annotation-Tool): Labeling tools for making CDEHP-Dataset.

## Team

<div class="row">
   <div class="cell">
      <img class="member_avatar" src="/assets/perry.jpg" alt="Zhanpeng Shao" />
      <p class="member_name"><a href="https://perryshao.github.io/">Zhanpeng Shao</a></p>
      <p>Associate Professor with College of Information Science and Engineering, Hunan Normal University. Specifically interested in activity understanding in videos.</p>
   </div>

   <div class="cell">
      <img class="member_avatar" src="/assets/xavier.jpg" alt="Wen Zhou" />
      <p class="member_name"><a herf="https://github.com/xavier-zw">Wen Zhou</a></p>
      <p>Obtained a Master's degree from Zhejiang University of Technology.</p>
   </div>

   <div class="cell">
      <img class="member_avatar" src="/assets/kuretru.jpg" alt="Wuzhen Wang" />
      <p class="member_name"><a href="https://github.com/kuretru">Wuzhen Wang</a></p>
      <p>Obtained a Master's degree from Zhejiang University of Technology, currently work for ByteDance.</p>
   </div>
</div>

## Contact

* If you have any questions, please raise an issue on the project's [Github repository](https://github.com/CDEHP-Dataset/cdehp-dataset.github.io/issues).
* If you are looking for related cooperation opportunities please contact [Prof. Z.P. Shao](https://perryshao.github.io/).
