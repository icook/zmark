# Zmark
=======


ZMark is a variant Implementation of [Bitmark](https://github.com/project-zmark/zmark/),
 a new tested implementation using Scrypt PoW.

ZMark benefits from being based on the 9.3 release of Bitmark, itself based on the  9.3 release of Bitcoin, with all BIPs unconditionally supported, all tests passing, and a clean code base.

Difficulty Adjustment Algortihm
--------------------------------
ZMark addresses the need for a more responsive difficulty adjustment algorithm,
implementing a variant of Dark Gravity Wave version 3, (DGWv3).


Block Reward Algorithm
--------------------------------

Additionally, ZMark refines the block-reward algorithm by matching coin emission to perceived demand for the coin. Current network hashrate is compared to a time-weighted average of recent hashrate peaks, which assigns greater weight to more recents peaks. Only when current hash rate is at least 1/4 of the modeled recent peak strength are subsidies set to the epoch's possible per-block maximum. Otherwise, block reward (or subsidy) is reduced proportionately, down to a as little as 1/20 of the epoch's maximum reward. 
 [See Table of Epochs with money-suppy growth (coin emission at max and min rates) curves, Appendix A]

For Bitmark, as of this and the previous implementation, the first _epoch_ will issue 7,880,000 (seven million eight hundred and eighty thousand) coins. Therefore the first epoch ever for Bitmark is still in its beginning, since less than 15% of this epoch's emission has been issued (as of January 2 2016 at 06:27 GMT is "blocks" : 55443, which, at the constant 20 BTM rate since inception will amount to: 1'108,860.00 BTM {one million one hundred and eight thousand eight hundred and sixty} {since blocks have invariably been 20 BTM/block subsidy since inception.); accordingly, the minimum reward will be for this epoch: 1 BTM (1/20 of 20) as the floor of the per-block reward and the maximum, when current hashrate is at least just 1/4 of _recent model peak's_ hashrate, is of course, 20 BTM. The reason  ?

Block quartering and halving as implemented in the original Bitmark code strictly limits total coin emission (money supply) to less than 27 million 580 thousand bitmarks ( 27,579,999.9927 BTM exactly). This limit is respected faithfully, but quartering and halvings are now triggered whenever money supply reaches the expected thresholds, which is not dependent any longer on the number of blocks, but rather, the total money supply (coins issued), since money supply is decoupled and not linearly dependent on number of blocks any longer.

Marking Facilities and App API Usage Reference Implementations
----------------------------------------------------------------

Marking: Digital Notary Service Facility DiNtService DigiNotesService DNTSvc : Federated Merkle Tree Hash Proof Root Insertion.



---------------------------------
For configuration details see the [wiki](https://github.com/zmark-project/zmark/wiki)

Just cloning? Clone pfennig, it's meant to be cloned.
