# Summary

The present release includes the Classical Armenian translation of the Gospels and the first ten chapters of the "History of the Armenians" by Movses Khorenatsi. The annotation of the Gospels results from a rule-based conversion from the PROIEL annotation, manually corrected and extended with additional information. The annotation of the "History of the Armenians" has been performed by a UDPipe2 annotator and manually corrected.

# Introduction

The present release includes a treebank of the Classical Armenian Gospels and the first ten chapters of the "History of the Armenians" by Movses Khorenatsi. The treebank results from a rule-based conversion of the <a href="https://github.com/proiel/proiel-treebank" target="_blank">PROIEL annotation</a> (see Dag T. T. Haug and Marius L. Jøhndal. 2008. 'Creating a Parallel Treebank of the Old Indo-European Bible Translations', in: Caroline Sporleder and Kiril Ribarov (eds.), Proceedings of the Second Workshop on Language Technology for Cultural Heritage Data (LaTeCH 2008) (2008), pp. 27-34). The PROIEL annotation is based on a digitalized version of Beda O. Künzle "Das altarmenische Evangelium" (Bern/Frankfurt am Main/New York: Peter Lang, 1984); https://titus.fkidg1.uni-frankfurt.de/texte/etcc/arm/armntbk/armnt.htm. The conversion from the PROIEL to UD annotation has been performed using a rule-based convertor (Petr Kocharov, Lilit Kharatyan). The conversion result has been manually corrected (Petr Kocharov) and extended with additional morphological features and relation subtypes, spelling in the Armenian alphabet, English glosses and sentence translations. The treebank of the "History of the Armenians" is based on the digital edition of the <a href="https://historians.armeniancathedral.org/index.htm" target="_blank">Arak29 Project</a>. The editions of Arak29 are adapted from the American University of Armenia’s Digital Library and other published sources. The morphological annotation of Arak29 has been automatically converted to UD with a rule-based convertor (Petr Kocharov, Lilit Kharatyan); the syntactic annotation is performed by a <a href="https://github.com/caval-repository/xcl_nlp/tree/main/parsers/UDPipe" target="_blank">UDPipe2 model</a> (<a href="https://github.com/caval-repository/xcl_nlp/blob/main/Kharatyan_Kocharov_2024_xcl_parsers.pdf" target="_blank">Kharatyan & Kocharov 2024</a>). All annotation has been manually corrected (Petr Kocharov).

# Acknowledgments

The treebank is developed by Petr Kocharov and Lilit Kharatyan at the University of Würzburg as part of the "CAVaL: Classical Armenian Valency Lexicon" project (PI Dr. Petr Kocharov), funded by the Deutsche Forschungsgemeinschaft (DFG), project number 518003859. We thank Professor Dr. Dag T. T. Haug and the PROIEL team for the permission to reuse the PROIEL annotation of the Classical Armenian Gospels for the purposes of the UD Classical Armenian-CAVaL treebank. We thank Dr. Daniil Kocharov (Tampere University) for advisory support and programming of the module for the processing of punctuation tokens for the convertor of the Gospels. We acknowledge the permission of the <a href="https://arak29.org/" target="_blank">Arak29 Charitable Foundation</a> for a non-commercial use of their digital editions of Classical Armenian texts.

# Data splits
The development data:
* Gospels: Matthew 4 and 5, Mark 4 and 5, Luke 3, 4 and 5, John 3, 4 and 5
* "History of the Armenians" by Movses Khorenatsi: Book 1: Chapter 10. 
The test data:
* Gospels: Matthew 6, 7 and 8, Mark 6 and 7, Luke 6, 7 and 8, John 6 and 7.
* "History of the Armenians" by Movses Khorenatsi: Book 1: Chapter 3.

# Changelog

* 2024-11-15 UD 2.15
  * First release of the fragment of the "History of the Armenians" by Movses Khorenatsi in UD
  * Fixed annotation errors
  * Improved tagsets for UPOS and features
  * Language-specific documentation for features have been added.
* 2024-05-15 UD 2.14
  * First release of the four Gospels in UD
  * Fixed annotation errors
  * The data is split into the train, test and dev sets.
  * Language-specific documentation for UPOS tags and the description of format extension have been added.
* 2023-11-15 UD 2.13
  * First release of the Gospel of Luke, chapters 1-12 in UD

## Format
UD_Classical_Armenian-CAVaL data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specifics:
* Sentence-level comments:
  * A unique sentence id `sent_id` contains reference to the document title, paragraph and sentence boundaries, e.g. `# sent_id = LUKE_1.1-4` for a sentence, which includes verses from 1 to 4 of the first chapter of the Gospel of Luke.
  * The transliteration of the sentence into Latin characters is provided in the `# transliterated_text...` comment. It is based on the transliteration system accepted in the _Revue des Études Arméniennes_.
  * The English translation of the sentence, based on the King James Bible, is provided in the `# translated_text...` comment.
* XPOSTAG column is currently not used.
* No enhanced dependencies or empty nodes present in DEPS column.
* MISC column has the following attributes:
  * `SpaceAfter=No`;
  * `Translit` and `LTranslit` for the transliterations of form and lemma (based on the transliteration system accepted in the _Revue des Études Arméniennes_);
  * `LId` for homonymous lemmas with coinciding UPOS;
  * `Gloss` for English glosses of lemmas.

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.13
License: CC BY-NC-ND 4.0
Includes text: yes
Genre: bible fiction
Lemmas: converted with corrections
UPOS: converted with corrections
XPOS: not available
Features: converted with corrections
Relations: automatic with corrections | converted with corrections
Contributors: Kocharov, Petr; Kharatyan, Lilit
Contributing: here
Contact: petr.kocharov@uni-wuerzburg.de
===============================================================================
</pre>
