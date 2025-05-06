# programming-homework-5-fx-carry-strategy-solved
**TO GET THIS SOLUTION VISIT:** [Programming Homework 5-FX Carry Strategy Solved](https://www.ankitcodinghub.com/product/programming-homework-5-fx-carry-strategy-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;97964&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Programming Homework 5-FX Carry Strategy Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

1 Introduction

An FX carry strategy borrows in a (low-interest-rate) currency and lends in another currency (with high interest rates). This is typically arranged via a cross-currency swap.

2 Data

Obtain 1M (0.08Y) rates for UK overnight index swaps (OIS) along with spot rates for the dollar versus pound1.

Obtain yield curves and FX rates of South African Rand, Thai Baht, Pakistani Rupee and Philippine Peso from the earliest possible date through now2. You may need to interpolate from sparser data in some cases. (Not all maturities are available in all currencies.)

3 Exercise

We will synthesize an approximate PL of weekly-traded cross-currency fixed- float swaps from the Libor rates and swap curves3, normalized to have a USD

1Available from 2009

2You may assume the data in Quandl’s YC dataset has swap curves, though in fact they are not quite the same.

3Use at least the 1, 2 or 3, and 5 year points.

1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
notional of US$10MM at the beginning of each week4. To keep bugs out of our cash flow tracking, we will convert flows to USD, though in some cases doing so is superfluous.

4 Fixed-Float Carry

In the borrowing (funding) currency, assume a rate of OIS+50bp, paid on 4/5 the notional amount (5x leverage) in the borrowing currency for each active position. In the lending currency, assume the schedule has a coupon every quarter at the 5Y swap rate, or (optionally) the 5Y treasury rate.

Weeks in which the 5Y swap rate of the lending currency is less than 50bp higher than the 5Y swap rate in the funding currency will be assumed to have no position

At the end of each week, assume you sell out of the position before opening a new one. You therefore need to tally accrued interest at the borrow and lend rates, and then compute mark-to-market for the swap exit.

4.1 Lending Currency

4.1.1 Mark to Market

Mark-to-market losses (due to swap rate and exchange rate changes) are the main source of downside deviation in this strategy.

Your original bond yield is the 5Y swap rate s5, as are the coupons. Use the new swap curve to form a corresponding zero-coupon bond curve, and reprice the bond (with its original coupons equal to s5) on the new interest rate curve, with the time remaining to all payments reduced by 1 week (or

1 of a year). 52

This is then converted (if necessary) to USD for buyback value at the new FX rate.

4You may forward fill in cases where you are testing weekly and only monthly data is available. If holidays interfere, delay a day or so as necessary, being sure to align data from the same day where possible. Wednesdays work best for weekly analysis.

2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
4.2 Borrowing Currency 4.2.1 Mark to Market

Here we can get a sufficiently good approximation just by assuming ∆V = 0, since the durations are so short.

4.2.2 Accrual

Our interest payment is one week at the funding rate, multiplied by our borrowed amount. We borrowed the funding-currency5 equivalent of $8MM at the starting FX rate f. We must now return that same amount of home currency at the new FX rate, plus 1 week of interest on it (also in home currency) at OIS + 50bp.

5 Analysis

Study and describe performance.

</div>
</div>
</div>
