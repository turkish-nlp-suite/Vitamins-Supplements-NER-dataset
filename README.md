# Vitamins and Supplements NER and Span Dataset

Turkish NER and Span dataset from customer reviews about supplemen and vitamin products. This dataset is scraped from Vitaminler.com.

This dataset is a multi-purpose Turkish NLU dataset containing customer reviews with entity and span annotations. Each dataset instance contains 

- a customer review
- a list of annotated entities and spans
- review id 

Here's an example annotation for you:

```
{
  "sent_id": 82838,
  "text": "Henüz 4 gündür kullanıyorum ama iyi geldi gibi.. bu kdr sürede anlaşılır mı bilmiyorum ama öğleden sonraları yaşadığım halsizliği enerji düşüklüğünü yaşamıyorum sanki. Sabah kahvaltıdan hemen sonra bir tablet alıyorum. Tabletler biraz büyük benim hap yutmada sorunum yok ama sorun yaşayanlar dikkat etsin...  iştahım da açılmadı...",
  "entities": [
      {
        "val": "halsizliği enerji düşüklüğünü yaşamıyorum",
        "label": "ETKİ",
        "start": 119,
        "end": 160
      },
      {
        "val": "bir tablet",
        "label": "DOZ",
        "start": 198,
        "end": 208
      },
      {
        "val": "iştahım da açılmadı",
        "label": "ETKİ",
        "start": 309,
        "end": 328
      }
  ]
}

```

The review id matches to the review_id in the mother dataset [Vitamin and Supplements Dataset](https://github.com/turkish-nlp-suite/Vitamins-Supplements-Reviews). You can fetch & match the product rating and more product infor from that dataset.

For this dataset we annotated both entities and spans. Span annotations are common in medical NLP datasets, spans capture the information about "what happens with the entity", i.e. more semantics about the entities in the text.
NER tags and their distribution are in the dataset are as follows:


|  Tag | Count |
|---|---|
| Disease  | 1.875   |
| Biomolecule  | 859  |
| User   | 634  |
| Other_product  | 543   |
| Recommender  | 436   |
| Dosage   | 471  |
| Brand  | 275  |
| User_demographics  | 192   |
| Ingredient   | 175  |
| Other_brand  | 121  |

Distribution of span tags:

|  Tag | Count |
|---|---|
| Effect  | 2.562  |
| Side_effect  | 608  |
| Taste_smell   | 558  |
| Health_complaints   | 858  |


All annotations are done by [Co-one](https://co-one.co/). many thanks to them for their contributions. 
This work is supported by Google Developer Experts Program. Part of Duygu 2022 Fall-Winter collection, "Turkish NLP with Duygu"/ "Duygu'yla Türkçe NLP". All rights reserved.  If you'd like to use this dataset in your own work, please kindly cite the paper [A Diverse Set of Freely Available Linguistic Resources for Turkish](https://aclanthology.org/2023.acl-long.768/):

```
@inproceedings{altinok-2023-diverse,
    title = "A Diverse Set of Freely Available Linguistic Resources for {T}urkish",
    author = "Altinok, Duygu",
    booktitle = "Proceedings of the 61st Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2023",
    address = "Toronto, Canada",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.acl-long.768",
    pages = "13739--13750",
    abstract = "This study presents a diverse set of freely available linguistic resources for Turkish natural language processing, including corpora, pretrained models and education material. Although Turkish is spoken by a sizeable population of over 80 million people, Turkish linguistic resources for natural language processing remain scarce. In this study, we provide corpora to allow practitioners to build their own applications and pretrained models that would assist industry researchers in creating quick prototypes. The provided corpora include named entity recognition datasets of diverse genres, including Wikipedia articles and supplement products customer reviews. In addition, crawling e-commerce and movie reviews websites, we compiled several sentiment analysis datasets of different genres. Our linguistic resources for Turkish also include pretrained spaCy language models. To the best of our knowledge, our models are the first spaCy models trained for the Turkish language. Finally, we provide various types of education material, such as video tutorials and code examples, that can support the interested audience on practicing Turkish NLP. The advantages of our linguistic resources are three-fold: they are freely available, they are first of their kind, and they are easy to use in a broad range of implementations. Along with a thorough description of the resource creation process, we also explain the position of our resources in the Turkish NLP world.",
}
```
