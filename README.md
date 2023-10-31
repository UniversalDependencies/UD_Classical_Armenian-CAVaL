# Summary

The present release includes a sample treebank of the first twelve chapters of the Classical Armenian translation of the Gospel of Luke (12963 tokens in 648 sentences) as part of the UD Classical Armenian-CAVaL treebank project. It results from a conversion of the PROIEL annotation of the Classical Armenian Gospels, then manually corrected and extended with additional information.

# Introduction

The present release includes a sample treebank of the first ten chapters of the Classical Armenian translation of the Gospel of Luke (10616 tokens in 539 sentences) as part of the UD Classical Armenian-CAVaL treebank project. The treebank results from a conversion of the PROIEL annotation of the Classical Armenian Gospels (https://github.com/proiel/proiel-treebank; see Dag T. T. Haug and Marius L. Jøhndal. 2008. 'Creating a Parallel Treebank of the Old Indo-European Bible Translations', in: Caroline Sporleder and Kiril Ribarov (eds.), Proceedings of the Second Workshop on Language Technology for Cultural Heritage Data (LaTeCH 2008) (2008), pp. 27-34). The PROIEL annotation is based on a digitalized version of Beda O. Künzle "Das altarmenische Evangelium" (Bern/Frankfurt am Main/New York: Peter Lang, 1984). The convertion from the PROIEL to UD annotation has been performed using a rule-based convertor developed as part of the "CAVaL: Classical Armenian Valency Lexicon" project, which is carried out at the University of Würzburg and funded by the Deutsche Forschungsgemeinschaft (PI Petr Kocharov, programmer Lilit Kharatyan). The convertion result has been manually corrected, adjusted to the UD annotation scheme, and extended a few with relation subtypes, spelling in the Armenian alphabet and English glosses. 

# Acknowledgments

The conversion has been performed by Petr Kocharov and Lilit Kharatyan at the University of Würzburg. We acknowledge the financial support of the Deutsche Forschungsgemeinschaft ("CAVaL: Classical Armenian Valency Lexicon" project, PI Dr. Petr Kocharov). We thank Professor Dr. Dag T. T. Haug and the PROIEL team for the permission to reuse the PROIEL annotation of the Classical Armenian Gospels for the purposes of the UD Classical Armenian-CAVaL treebank. We thank Dr. Daniil Kocharov (Tampere University) for advisory support and programming of the module for the processing of punctuation tokens. We thank Thomas J. Samuelian for the permission to reuse the English glosses of the electronic concordance of the Armenian Bible (https://bible.armeniancathedral.org/).

## Format
UD_Classical_Armenian-CAVaL data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specifics:
* Sentence-level comments:
  * A unique sentence id `sent_id` contains reference to the document title, paragraph and sentence boundaries, e.g. `# sent_id = LUKE_1.1-4` for a sentence, which includes verses from 1 to 4 of the Gospel of Luke.
  * The transliteration of the sentence into Latin characters is provided in the `# transliterated_text...` comment.
  * The English translation of the sentence, based on the King James Bible, is provided in the `# translated_text...` comment.
* XPOSTAG column is currently unused.
* No enhanced dependencies or empty nodes present in DEPS column.
* MISC column has the following attributes:
  * `SpaceAfter=No`;
  * `Translit` and `LTranslit` for the transliterations of form and lemma (based on on the transliteration system accepted in the _Revue des Études Arméniennes_);
  * `LId` for homonymous lemmas;
  * `Gloss` for English glosses of lemmas.

# Changelog

<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.13
License: CC BY-SA 4.0
Includes text: yes
Genre: bible
Lemmas: converted with corrections
UPOS: converted with corrections
XPOS: not available
Features: converted with corrections
Relations: converted with corrections
Contributors: Kocharov, Petr; Kharatyan, Lilit
Contributing: here
Contact: petr.kocharov@uni-wuerzburg.de
===============================================================================
</pre>
