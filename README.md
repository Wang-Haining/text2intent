![icon](https://github.com/Wang-Haining/text2intention/blob/master/img/text2intention.png)
# speech-acts-classifier

A speech acts classifier based on pre-trained models.

# 1. Step 1: A toy system with existing tagged copora

### possible useful corpus
- [Switchboard Dialog Act Corpus](https://convokit.cornell.edu/documentation/switchboard.html)
    - [overview](http://compprag.christopherpotts.net/swda.html)
    - [manual](https://web.stanford.edu/~jurafsky/ws97/manual.august1.html)

- [The NPS Chat Corpus](http://faculty.nps.edu/cmartell/npschat.htm)
    - [overview](http://faculty.nps.edu/cmartell/npschat.htm)

- [Meeting Recorder Dialogue Act Corpus](https://github.com/NathanDuran/MRDA-Corpus)
    - [manual](https://github.com/NathanDuran/MRDA-Corpus/blob/master/mrda_manual.pdf)
    - [competition on this corpus](https://paperswithcode.com/sota/dialogue-act-classification-on-icsi-meeting)

### papers

- [Tweet Acts: A Speech Act Classifier for Twitter](https://arxiv.org/pdf/1605.05156.pdf)
- [Automated Speech Act Categorization of Chat Utterances in Virtual Internships](https://educationaldatamining.org/files/conferences/EDM2018/papers/EDM2018_paper_115.pdf)
- [Dialogue Act Recognition via CRF-Attentive Structured Network](https://arxiv.org/pdf/1711.05568v1.pdf)
- [Classifying Speech Acts using Verbal Response Modes](https://www.aclweb.org/anthology/U06-1007.pdf)

# 2. Step 2: A customized algorithm classifying a speech acts tagset

The goal in this phrase is to achieve CMC-schema tagging with a reasonal F score. Because assigning three tags (perspective/bona fide/intention) is a multi-task learning and more challenging than other tasks.

- candidate tagsets:
    - Austin (1962)
    - Bach & Harnish (1979) 
    - Francis & Hunston (1992) 
    - CMC schema (Herring, Das, & Penumarthy, 2005)

# 3. Step 3: Developing a semi-supervised learning framework user-friendly to sociolinguists

- a user can directly use an already fine-tuned pre-trained model on CMC and three dialog act tagsets

- or user can define their own schema
    - then let user tag a part of their own corpus based on their schema
    - the framework fine-tunes the pretrained model and report the accuracy, recall, and F score. Hide details to users.

# 4. Step 4: Deploying

TBD, but online is preferred.









