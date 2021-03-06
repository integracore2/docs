# Staking and Payouts

## Motivation

How do we design a payout system that incentive aligned and resistant against [sybil attacks](https://en.wikipedia.org/wiki/Sybil_attack)? 

The answer is staking.

Numerai wants accurate predictions and is willing to reward it. How much you can earn/burn is a function of your performance and stake. This is also known as having [skin in the game](https://www.amazon.com/dp/B075HYVP7C/).    

Staking also gives Numerai a sybil resistant way to allocate payouts. Since payouts are a percentage of your stake value, you cannot game the payout system by simply creating duplicate accounts.

{% hint style="success" %}
What would the internet look like if every interaction was staked? Read more at [erasure.world](https://erasure.world/)
{% endhint %}

## Managing your stake

You can manage your stake on the Numerai website by opening the staking modal. Use this modal to increase or decrease your stake amount, or switch your stake type between `corr` and `mmc`.

![staking modal](../.gitbook/assets/image%20%2844%29.png)

Increasing your stake will take NMR from your wallet and put it into the stake. Decreasing will take NMR from the stake and back into your wallet.

Changes to your stake do not apply immediately, instead they apply on the `effective_date` as shown on the right.

* Switching between `corr` and `mmc` applies next `Thursday`
* Increases apply next `Thursday`
* Decreases impact your `stake amount`next Thursday,  but the funds are only released after next `Thursday + 4 weeks`

## Payouts

The payout for each round is based on your `stake_value` as of the first Thursday after the submission deadline. Payouts are rolled back into your stake value at the beginning of the next round on Thursday. 

For example, if your `stake_value` on round N is `100`, and your `correlation = 0.05`, then your payout will be `+ 5NMR`, which will be applied to your stake value in round N+4.  

{% hint style="warning" %}
Decreasing your stake will lower your `stake_value` in the immediate next round, even though the decrease will only happen 4 weeks later.
{% endhint %}

{% hint style="info" %}
If you decide to cancel your decrease request, your stake value will go back up to the original value in the immediate next round.
{% endhint %}

## Compounding

Since there is a new round every week and each round lasts 4 weeks, stake values compound with a 4-week delay.

For example, the stake value of week 6 is based on the previous stake value of week 5 \(110 NMR\) + the payout from week 2 \(-5 NMR\) = 105 NMR.

![stake compounding](https://documents.app.lucidchart.com/documents/2cb7265f-6e5b-454a-a84d-6f32b6058f34/pages/0_0?a=466&x=249&y=136&w=1112&h=486&store=1&accept=image%2F*&auth=LCA%20a086c3be9ef17d9fa2cd22ee9808e742d1a2d888-ts%3D1590449860)

## Abuse

We reserve the right to refund your stake and void all earnings and burns if we believe that you are actively abusing or exploiting the payout rules.

We will rarely ever exercise this right, as our payout systems are designed to be attack resistant, and we want users to try new ideas without fear of punishment.

If we do detect abuse, we will inform the community about it and explain the actions we take against it. Here is [one example](https://forum.numer.ai/t/leaderboard-bonus-exploit-uncovered/200/8). 

