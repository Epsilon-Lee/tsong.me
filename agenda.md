---
layout: blank
---

## Agenda

### Apr 10
Use more computational resources to finish the Tabular Experiment.
The code is available on [https://github.com/jiamings/TabularRLpp](https://github.com/jiamings/TabularRLpp).

#### Azure usage
Currently using 7 instances, D3v2-Promo, D12v2-Promo, D2v2-Promo + 4 F8S.

I find that F8S are cheaper to use since we demand much more CPU than memory.

The jobs that are currently running are [here in this Google doc](https://docs.google.com/document/d/1BziGK-xzp9pLw3hlqdOh4PJQrdHevYJc7J-t9uxej_8/edit?usp=sharing). They should be ready sometime on Wednesday.



### Apr 12

Interestingly, the UBEV-EB results does not seem to be better than MBIE-EB for 100 states under the parameters I select. (Average of 10 runs)

[https://github.com/jiamings/TabularRLpp/blob/master/visualization.ipynb](https://github.com/jiamings/TabularRLpp/blob/master/visualization.ipynb)

I am trying 0.75 and 0.35 to see if UBEV-EB performance can be improved.

The results for 200 should be ready by tomorrow afternoon. It seems that the speed is larger than quadratically increasing, so running 1 million episodes takes longer than expected.



### Apr 14

Chris said that MIBE-EB and UBEV-EB should not be too different since the llnp term would be too small - the two intervals only differ by a constant. He also said that it might be helpful to try to update once every 10 episodes.



### Apr 16

UBEV does not seem to perform much better than MBIE even with 10 million episodes...

![](public/img/agenda/mbie_ubev.png)

I think the implementation should be correct, since Chirs showed me similar results on chain with 50 states.