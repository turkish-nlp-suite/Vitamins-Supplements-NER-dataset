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
This work is supported by Google Developer Experts Program. Part of Duygu 2023 Fall-Winter collection, "Turkish NLP with Duygu"/ "Duygu'yla Türkçe NLP". All rights reserved.
