---
layout: post
title: Methodology
permalink: /methodology/
---

Papers were downloaded from PDFs from the publisher's sites. The PDFs were processed with [GROBID](https://github.com/kermitt2/grobid){:target="_blank"}, a machine learning library that parses PDF documents into structured XML documents. It's a really powerful and surprisingly accurate parser for scientific documents, including functionality to recognize, parse, and Crossref-verify references. The abstracts and body texts were extracted after removing references to citations and figures. For journals without abstracts, the first paragraph was taken to be the abstract.

The two-axis text plot was created with [scattertext](https://github.com/JasonKessler/scattertext){:target="_blank"}, a truly awesome and rich package with support for a large variety of analyses, most of which I have not used for the PoTY project. Visualization of associations for phrases was done with [pytextrank](https://github.com/DerwenAI/pytextrank){:target="_blank"} as part of a [spaCy pipeline](https://spacy.io/universe/project/spacy-pytextrank){:target="_blank"}.

For topic models, the text was tokenized and stemmed using a Snowball stemmer and stopwords included with the [NLTK (Natural Language Toolkit)](https://www.nltk.org/){:target="_blank"} package. We use the Latent Dirichlet Allocation (LDA) model from [tomotopy](https://bab2min.github.io/tomotopy/v/en/){:target="_blank"}. Visualization of the topic models were achieved with [pyLDAvis](https://github.com/bmabey/pyLDAvis){:target="_blank"}, which is the Python implementation of the R-based [LDAvis](https://nlp.stanford.edu/events/illvi2014/papers/sievert-illvi2014.pdf){:target="_blank"}.

Geographies were processed with the [Geocoder](https://github.com/kermitt2/grobid){:target="_blank"} package, using the [ArcGIS provider](https://developers.arcgis.com/rest/geocode/api-reference/overview-world-geocoding-service.htm){:target="_blank"}. The map was generated with [Folium](https://python-visualization.github.io/folium/index.html){:target="_blank"}.
