# LLM_FineTuning


# science_qna

This fine tunes a pretrained question and answering LLM to specifically answer questions in science and general knowledge. We fine tune the pretrained model on the ScienceQA data set so that given a question and context of the expected answer, the LLM generates the most likely answer from the context or choices. LLM question answering models can be broadly categorized into extractive, open generative, and closed generative QA, each with distinct approaches for extracting or generating answers based on context or internal knowledge. The LLM QA implemented in science_qna is Extractive QA where models receive a question and a context (e.g., text, tables, or HTML) and extract the answer directly from the provided context. This is useful for Information retrieval. 

# art_commenter

The SemArt data set is a data set of artwork and corresponding textual comments. The comments are less of a reviewers critique of the work and more of a curator's descriptive comments about the artwork, such as its origin, who created or made it, and at times, some comments about the art such as the scene being depicted or some some comments about the persons in the artwork. To see how we can obtain an LLM that provides similar comments about such art work, we utilize a pre-trained BLIP image captioning model, and fine tune it with the SemArt data. It is expected that the pretrained BLIP model would give our fine-tuning a head start in image recognition and understanding and also assigning textual descriptions. The fine tuned model performs well, most times being able to generate surprisingly good descriptions of test SemArt images.  

# agent_article_researcher

Given an article, this agentic app uses an LLM to extract all statements and/or assertions. Another LLM then generates counterfactuals or hypothesis to each of the extracted statements. These counterfactuals could be new ideas or research pathways. The next thing then is to fact check these counterfactual hypothesis to see if they pass a minimal factuality or validity test by cross-checking them with a wikipedia LLM that is queried to see if the counterfactual hypothesis go against any known knowledge facts. The agentic_article_researcher can be a basis for developing a deep research agent 

# Data and models
Data and the fine tuned models are available at Hugging Face:https://huggingface.co/shaddie

