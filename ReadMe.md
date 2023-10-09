iTTS.py [![Unlicensed work](https://raw.githubusercontent.com/unlicense/unlicense.org/master/static/favicon.png)](https://unlicense.org/)
===========
~~![GitLab Build Status](https://gitlab.com/KOLANICH/iTTS.py/badges/master/pipeline.svg)~~
~~![GitLab Coverage](https://gitlab.com/KOLANICH/iTTS.py/badges/master/coverage.svg)~~
[![Libraries.io Status](https://img.shields.io/librariesio/github/KOLANICH/iTTS.py.svg)](https://libraries.io/github/KOLANICH/iTTS.py)
[![Code style: antiflash](https://img.shields.io/badge/code%20style-antiflash-FFF.svg)](https://codeberg.org/KOLANICH-tools/antiflash.py)

**We have moved to https://codeberg.org/KOLANICH-tools/iTTS.py , grab new versions there.**

Under the disguise of "better security" Micro$oft-owned GitHub has [discriminated users of 1FA passwords](https://github.blog/2023-03-09-raising-the-bar-for-software-security-github-2fa-begins-march-13/) while having commercial interest in success of [FIDO 1FA specifications](https://fidoalliance.org/specifications/download/) and [Windows Hello implementation](https://support.microsoft.com/en-us/windows/passkeys-in-windows-301c8944-5ea2-452b-9886-97e4d2ef4422) which [it promotes as a replacement for passwords](https://github.blog/2023-07-12-introducing-passwordless-authentication-on-github-com/). It will result in dire consequencies and is competely inacceptable, [read why](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

If you don't want to participate in harming yourself, it is recommended to follow the lead and migrate somewhere away of GitHub and Micro$oft. Here is [the list of alternatives and rationales to do it](https://github.com/orgs/community/discussions/49869). If they delete the discussion, there are certain well-known places where you can get a copy of it. [Read why you should also leave GitHub](https://codeberg.org/KOLANICH/Fuck-GuanTEEnomo).

---

Just a kernel for Jupyter notebook speaking text from cells.

The work is based on https://github.com/takluyver/bash_kernel, which is licensed under [BSD 3-clause license](https://github.com/takluyver/bash_kernel/blob/master/LICENSE).

Limitations and ToDos
======================

* Currently it speaks only using system loudspeakers because speech-dispatcher (and its protocol) lacks the functionality to get the voice stream instead of speaking it.
* Currently lacks an abstraction layer to support different APIs, such as SAPI5 uniformly.
* Currently it lacks automatic language detection. `langdetect` is shit (in the sense its quality is too poor). `nltk` can be used for that once the issue with insecure way of providing pretrained models needed for it is solved.
* Currently it lacks autocompletion of the arguments of the magics.
* Currently it lacks hints on the magics.
* Currently it lacks autocompletion of words for usual text based on beginning of the sentence.
    * Markov models can be used
    * or maybe RNNs
