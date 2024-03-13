<h1 align="center">LupusNet</h1>
<h4 align="center">	
Lupus Nephritis Subtype Classification with only Slide Level Labels</h4>
<p align="center">
<strong>Authors:</strong> Amit Sharma, Ekansh Chauhan, Megha S Uppin, Liza Rajasekhar, C V Jawahar, P K Vinod
<br>
<br>
<a href="https://www.medrxiv.org/content/10.1101/2023.12.03.23299357v1">medRxiv</a> | <a href="https://hai.iiit.ac.in/ipd/">India Pathology Dataset Website</a> | <a href="#cite">Cite</a>
</p>
<!-- <a href="https://github.com/elangosundar/awesome-README-templates/blob/master/LICENSE"><img src="https://img.shields.io/github/license/elangosundar/awesome-README-templates?color=2b9348" alt="License Badge"/></a> -->
<hr>
<strong>Abstract:</strong> Lupus Nephritis classification has historically relied on labor-intensive and meticulous glomerular-level labeling of renal structures in whole slide images (WSIs). However, this approach presents a formidable challenge due to its tedious and resource-intensive nature, limiting its scalability and practicality in clinical settings. In response to this challenge, our work introduces a novel methodology that utilizes only slide-level labels, eliminating the need for granular glomerular-level labeling. A comprehensive multi-stained lupus nephritis digital histopathology WSI dataset was created from the Indian population, which is the largest of its kind. LupusNet, a deep learning MIL-based model, was developed for the subtype classification of LN. The results underscore its effectiveness, achieving an AUC score of 91.0%, an F1-score of 77.3%, and an accuracy of 81.1% on our dataset in distinguishing membranous and diffused classes of LN.
<br>
<br>
<a href="https://www.medrxiv.org/content/10.1101/2023.12.03.23299357v1" alt="Read full text"><img src="images\arch.png" style="border: 1px solid grey; padding: 5px; margin: 5px"></a>


## 👨🏻‍💻 Code
We have adapted our pipeline from [CLAM](https://github.com/mahmoodlab/CLAM?tab=readme-ov-file#reference).
```
CUDA_VISIBLE_DEVICES=0 python main.py --drop_out --early_stopping --lr 2e-4 --k 10 --label_frac 0.5 --exp_code ln4_vs_ln5_lupusnet --weighted_sample --bag_loss ce --inst_loss svm --task ln4_vs_ln5 --model_type clam_sb --log_data --data_root_dir DATA_ROOT_DIR
```


## :book: Cite
<p id="cite"></p>

```
@inreview{
    lupusnet,
    title={LUPUS NEPHRITIS SUBTYPE CLASSIFICATION WITH ONLY SLIDE LEVEL LABELS}, 
    DOI={10.1101/2023.12.03.23299357},
    author={Sharma, Amit and Chauhan, Ekansh and Uppin, Megha S and Rajasekhar, Liza and Jawahar, C V and Vinod, P K},
    year={2023}
}
```

## :pencil: License

© This code is made available under the GPLv3 License and is available for non-commercial academic purposes.

