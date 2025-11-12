Used the following frames to generate candidate words at [https://sarablalockng.github.io/research/elicitations/make_wc.html](https://sarablalockng.github.io/research/elicitations/make_wc.html):

```
T N
VX1 L T AH0 N
VX1 N T AH0 N
VX1 R T AH0 N
VX1 T AH0 N
EH L #|CX
IY L #|CX
EY L #|CX
```

There are sorted and unsorted variants of these word candidates, where the sorting is done according to the lexical frequency from [English Gigaword Fifth Edition](https://catalog.ldc.upenn.edu/LDC2011T07).

The variants all_words and all_words sorted combine the words from all t-glottalized frames.

The gigaword frequencies are stored as an ordered list called `cmu_ordered_by_frequency` in the file `cmu_freq.py`.

The code can be rerun with the invocation `python3 sort_by_freq.py`.

The script make_word_pairs.py selects pairs of words by first collapsing multiple senses into their highest-ranked entry, and then returns the two closest-ranked words in each category and the difference in their rank.

To test word pairs, use [this notebook](https://colab.research.google.com/drive/1wNXyLsL4dySnmSEw0_W9fRRkRK6-rea2?usp=sharing), which computes probabilities from GPT2.

Info for the model used as of 11/12/25:
```
ModelInfo(id='openai-community/gpt2', author='openai-community', sha='607a30d783dfa663caf39e06633721c8d4cfcd7e', created_at=datetime.datetime(2022, 3, 2, 23, 29, 4, tzinfo=datetime.timezone.utc), last_modified=datetime.datetime(2024, 2, 19, 10, 57, 45, tzinfo=datetime.timezone.utc), private=False, disabled=False, downloads=11770237, downloads_all_time=None, gated=False, gguf=None, inference=None, inference_provider_mapping=None, likes=3014, library_name='transformers', pipeline_tag='text-generation', mask_token=None, card_data={'base_model': None, 'datasets': None, 'eval_results': None, 'language': 'en', 'library_name': None, 'license': 'mit', 'license_name': None, 'license_link': None, 'metrics': None, 'model_name': None, 'pipeline_tag': None, 'tags': ['exbert']}, transformers_info=TransformersInfo(auto_model='AutoModelForCausalLM', custom_class=None, pipeline_tag='text-generation', processor='AutoTokenizer'), trending_score=None, safetensors=SafeTensorsInfo(parameters={'F32': 137022720}, total=137022720), security_repo_status=None, xet_enabled=None)
```
