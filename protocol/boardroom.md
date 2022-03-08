# Boardroom

## The Boardroom User Interface

![The Boardroom user interface](<../.gitbook/assets/Screenshot 2022-01-26 193115.png>)

Let's take a look at each element of the Boardroom user interface and what it means.

1. **NEXT EPOCH**\
   The amount of time remaining until the next epoch.
2. **CURRENT EPOCH**\
   The number of the current epoch.
3. **BRRRR PEG (TWAP)**

&#x20;      The TWAP (time-weighted average price) of the BRRRR peg. The Boardroom only mints new              BRRRR as rewards for BRRRRSHARE stakers when this value is above 1.01 at the end of the current epoch.

&#x20;  **4. APR**\
&#x20;      The yield for BRRRRSHARE stakers in the Boardroom if the Boardroom was printing every epoch. This calculation is based on the last recorded print in the Boardroom.

&#x20;   **5. BRRRRRSHARES STAKED**\
&#x20;      The total amount of BRRRRSHARE currently staked in the Boardroom.

&#x20;   **6. BRRRR Earned**\
&#x20;      The amount of BRRRR you've earned as rewards for staking BRRRRSHARE in the Boardroom.

&#x20;   **7. BSHARE Staked**\
The amount of BRRRRRSHARE you currently have staked in the Boardroom.

### Boardroom Specifications

* Epoch duration: 6 hours
* Any interaction with the Boardroom (staking/unstaking BRRRRSHARE or withdrawing BRRRR rewards) will **lock your staked BRRRRRSHARE for 6 epochs and BRRRR rewards for 3 epochs.**
*   Distribution of BRRRR during expansion (Boardoom printing):

    **X%** goes to Boardroom BSHARE stakers as rewards

    **X%** goes to DAO fund

    **X%** goes to dev fund
* Epoch Expansion: The current expansion cap is based on the currently circulating BRRRR supply (see [BRRRR Distribution ](bomb-distribution.md)for details). If there are bonds to be redeemed, 65% of minted BRRRR goes to the treasury until its sufficiently stocked to satisfy future bond redemption.

{% hint style="info" %}
Note that the Boardroom **does not** print any rewards for BRRRRSHARE stakers when the Boardroom TWAP < 1.01.
{% endhint %}

## Boardroom FAQ

****

1. **Once BRRRR are issued, does the Boardroom stop printing BRRRR until we are above peg again?**&#x20;

Staking BRRRRSHARE will only give you BRRRR rewards when the price of BRRRR is above the peg (10,000 BRRRR to 1 BNB), but not when it is under the peg.

**2. What happens if I interact with the Boardroom in any way?** **Are there any lockup periods?**&#x20;

Yes, there are two lockup timers. One for BRRRR rewards and one for staked BRRRRSHARE. Any interaction with the Boardroom will reset both timers. The lockup period for withdrawing BRRRR rewards is 3 epochs (18 hours), or 6 epochs (36 hours) to unstake your BRRRRSHARE.&#x20;

**3.** **Are the Boardroom rewards pro-rated by time? For example, if I stake three hours before the end of an epoch versus five hours before the end of an epoch, would I get different rewards?**

No, Boardroom rewards are determined by how much you have staked at the time of printing (i.e., at the end of one epoch and the start of the other). It doesn't matter if you stake three hours before or thirty seconds before the emissions occur.

**4. If I remove my BRRRRSHARE from the Boardroom without first collecting my BRRRR, will they be lost forever?**&#x20;

No, they will still be there to collect whenever you need.

**5. The Boardroom APR dropped because we're in a "debt phase." What does that mean?**&#x20;

A debt phase takes place during expansion epochs that start after a contraction period where there are still BRRRRBOND to be redeemed. 65% of expansion during a debt phase is allocated to the treasury fund to prepare for subsequent BRRRRBOND redemption down the road. This amount is always reserved, regardless of whether BRRRRBOND holders are redeeming bonds or not. Once enough BRRRR are sufficiently stocked in the treasury to satisfy the redemption of all circulating BRRRRBOND, expansion rates will resume to normal.

**6. If we're in a debt phase, how long will it last until the Boardroom continues printing as normal?**

The debt phase will last as long as is necessary to adequately pay back outstanding BRRRRBOND debt. Please keep in mind that the DAO will also need to collect a little extra, as there needs to be a cushion to cover the bonus premiums when people redeem BRRRRBOND over peg.\
\
There's no exact way of calculating how many epochs it will take, since the protocol doesn't know exactly when people will redeem their BRRRRBOND. The debt phase cannot end until the treasury has enough BRRRR to cover the redemption of all outstanding BRRRRBONDs plus a premium.

**7. At the end of the epoch, the Boardroom did not print BRRR, but then no BRRRRBOND(s) were issued either. Why?**

There is a balanced state "at peg" when BRRRR's TWAP is between 1.00 and 1.01, which results in no contraction or expansion of the circulating supply of BRRRR. This is referred to as a zen epoch

**8. If BRRRR continues to climb above the price of the peg, will that influence how long the debt phase lasts?**

Depending on the price of BRRRR, the Boardroom print will have to adjust to provide a buffer for any unclaimed BRRRRBOND. As the price of BRRRR climbs above the peg, more BRRRR needs to be distributed to the treasury to account for BRRRRBOND redemption plus premiums.

**9. How can I figure out what my future BRRRR rewards will be from the Boardroom?**

Let's take a look at a simplified example for a non-debt phase: say you have 1 BRRRRSHARE staked out of 10 total BRRRRSHAREs staked in the Boardroom. In this case, you will receive 10% of the total BRRRR printed in the Boardroom.

For this example we are assuming that there is a total circulating supply of 10,000 BRRRR and the current expansion rate is at 4%, so a total of 400 BRRRR will be printed in the Boardroom. Under the protocol's current rules, 60% of those newly printed BRRRR will be distributed to BRRRRSHARE stakers in the Boardroom. (See the[ BRRRR Distribution](https://contact-equilibrrrrium.gitbook.io/protocol/protocol/bomb-distribution) page for more details on how BRRRR is distributed within the protocol.)

\
Therefore, you would get: ((0.04 \* 10000) \* 0.6) \* (1/10) = 24 BRRRR

Thus, the formula to calculate your rewards is as follows:\
\
**((ExpansionRate \* CirculatingBRRRRSupply) \* 0.6) \* (YourBRRRRShareStake / TotalBRRRRShareStaked)**

**10. How long will it take for BRRRRSHARE to pay itself off from BRRRR rewards based on current prices?**

This will vary constantly as the APR in the Boardroom fluctuates, along with other variables such as the price of BRRRR.

For a quick estimation, however, you can do the following:

1. Take the total APR shown in the Boardroom and divide that by 365 to get the daily APR. (For this example we will say the daily APR is 5%.) 
2. Multiply that daily APR by the current market price of the total BRRRRSHARE you have staked to see what your daily rewards are. (In this example, we have 5 BRRRRSHARE, each worth $500, for a total amount staked of $2500. Your daily return in this case would be $2500 \* 0.05, which comes out to $125 per day.)
3. Take your initial buy-in price for BRRRRSHARE and divide it by your daily rewards. If you bought these 5 BRRRRSHARE at a higher price, say $700 for example, in the current market conditions you would recover your initial investment of $3500 in 3500/125 or 28 days.
