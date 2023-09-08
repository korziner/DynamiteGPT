# DynamiteGPT
List articles with code and fast growing public datataset using LLM. 
AI_Talent_Hub2023 product


Demo https://2b95cc7bef0e99b5cb.gradio.live (link expires in 72 hours)


LLM reads all articles to the its vector DB:

legal alternative to sci-hub.tw is Unpaywall.

We harvest content directly from over 50,000 journals and open-access repositories from all over the world. We also use great open data from PubMed Central...
https://opendata.stackexchange.com/questions/7084/bulk-download-sci-hub-papers


It'll take up roughly 300GB of disk space.

    aws s3 sync "s3://openalex" "openalex-snapshot" --no-sign-request

https://docs.openalex.org/download-all-data/download-to-your-machine
