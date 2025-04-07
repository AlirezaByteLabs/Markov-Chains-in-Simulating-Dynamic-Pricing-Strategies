---
# You can also start simply with 'default'
theme: Seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: ./assets/cover_bg.webp
# some information about your slides (markdown enabled)
title: ارائه درس شبیه سازی
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
dir: rtl
addons:
  - slidev-addon-rabbit
  - fancy-arrow

rabbit:
  slideNum: true
---

# Markov Chains & Dynamic Pricing
## Airline Ancillary Offer Optimization

<!--
ancillary: خذمات جانبی
-->

امیر حسین دشتی و علیرضا قبادی، ۱۴۰۴/۰۱/۱۹

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
<carbon:arrow-right />  اسلاید بعدی 
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->
---
dir: rtl
transition: fade-out
---

# موضوعات مورد بحث
کامل شود با فرمت لیست

---
layout: section
---

# تعاریف اولیه

در این بخش به ارائه اصطلاحات  مورد استفاده در ارائه خواهیم پرداخت.


---
dir: rtl
---

# تعاریف اولیه

## Offer
منظور از offer یک پیشنهاد برای خرید است که احتمالا با قیمت ارزان‌تر از قیمت مورد انتظار خواهد بود. یک پیشنهاد می‌تواند به صورت bundle(ترکیبی از چند محصول) یا تکی باشد.

---
layout: section
dir: rtl
---

# مقدمه

در این بخش شروع به توضیح مسئله و تشریح آن می‌پردازیم.

---
transition: fade-out
dir: rtl
src: ./pages/introduction.rtl.md
---

some text

---
layout: fact
dir: rtl
transition: slide-down
---

<strong>
احتمال خرید یک پیشنهاد، فقط به قیمت اون پیشنهاد وابسته نیست. بلکه به قیمت <span data-id="customers-rights" v-mark.green="1">سایر پیشنهادات</span> در سبد پیشنهادات برای مشتری نیز بستگی دارد
</strong>

<FancyArrow v-click="2" q1="[data-id=customers-rights]" pos1="bottom" q2="[data-id=customers-wrongs]" head-size="30" pos2="top" color="teal" width="4" roughness="3" arc="0.1" seed="1" />

<br>
<br>
<br>

<span v-click="2" color="red">
<span data-id="customers-wrongs">
مشتری 
</span>
زمانی که یک آفر دریافت می‌کنه اون رو با جایگزین‌های موجود مقایسه می‌کنه
</span>

<style>
strong {
  font-size: xx-large;
}
</style>


---
layout: section
dir: rtl
---

# توضیح کسب درآمد صنعت هواپیمایی

در زمان گذشته، حال، آینده

---
layout: section
dir: rtl
---

## گذشته و حال


---
dir: rtl
transition: fade
---
از سال ۲۰۰۰ به بعد، دو مدل اصلی در فروش بلیط هواپیما ظهور کرد:

<div v-click="1" v-motion
  :initial="{ x: -50 }"
  :enter="{ x: 0 }"
  :leave="{ x: 50 }"
>

## خطوط هوایی کامل (Full-Service Airlines)
  - فروش بلیط به صورت بسته‌بندی شده (باندل)
  - خدمات جنبی مانند بار مجانی، غذا و انتخاب صندلی به‌صورت پیش‌فرض در قیمت بلیط گنجانده می‌شد.
  - مدل درآمدی مبتنی بر قیمت ثابت و خدمات یکپارچه.

## خطوط هوایی کم‌هزینه (Low-Cost Carriers - LCCs)
- فروش بلیط پایه به صورت جدا از خدمات اضافی
- خدمات جانبی (اضافه‌بار، غذا، صندلی) به صورت اختیاری و با هزینه جداگانه ارائه می‌شد.
- حق انتخاب بیشتر برای مسافر و مدل درآمدی انعطاف‌پذیر.

</div>

---
dir: rtl
transition: fade
---

## همگرایی دو مدل کسب‌وکار
با گذشت زمان، هر دو گروه به سمت یکدیگر حرکت کردند:

- شرکت‌های کم‌هزینه با مشاهده موفقیت مدل باندل، شروع به ارائه پکیج‌های ترکیبی کردند تا مشتریان خطوط سنتی را جذب کنند.
- خطوط هوایی سنتی برای رقابت با شرکت‌های ارزان‌قیمت، فروش تک‌خدمات (Unbundled) را آغاز کردند تا به مسافران انعطاف بیشتری بدهند.
- امروز، مرز بین این دو مدل کمرنگ شده و بسیاری از شرکت‌ها ترکیبی از هر دو استراتژی را به کار می‌گیرند تا پاسخگوی نیازهای متنوع مسافران باشند.


---
layout: section
dir: rtl
---

## ایده برای آینده

 شرکت‌های هواپیمایی برای تحقق هدف ایجاد پیشنهادهای پویا، می‌خواهند مجموعه‌ای از پیشنهادات را ارائه دهند که متناسب با درخواست مشتری و شرایط سفر، هم از نظر محتوا و هم از نظر قیمت، سازگار بوده و در تمام کانال‌های دریافت پیشنهاد یکسان باشد.

---
dir: rtl
layout: two-cols
class: text-center
---

<template v-slot:default>

# توضیع فعلی محصولات

<img src="./assets/airline_market_system_letf.png"/>

</template>
<template v-slot:right>

# ویژگی‌ها

<v-clicks>

- مشتریان با مجموعه‌ای از <span v-mark.green="1"> صفحات فروش ثابت </span> مواجه می‌شوند.
- <span v-mark.red="2">پیشنهادهای</span> ارائه شده (محصولات و قیمت‌ها) برای همه مشتریان <span v-mark.red="2">یکسان</span> هستند.
- پیشنهادها بر اساس نیازها یا سابقه خرید مشتریان <span v-mark.blue="3">شخصی‌سازی نمی‌شوند.</span>
- این روش فرصت ارائه <span v-mark.yellow="4">پیشنهادهای مکمل</span> و افزایش فروش را از دست می‌دهد.

</v-clicks>

</template>

<style>
  .grid-cols-2 {
    column-gap: 10px;
  }
</style>


---
dir: rtl
layout: two-cols
class: text-center
---

<template v-slot:default>

# پیشنهادات پویا


<img src="./assets/airline_market_system_right.png"/>

</template>
<template v-slot:right>

# ویژگی‌ها

<br>
<br>

- قیمت‌ها و پیشنهادات بسته به <span v-mark.green="0">زمینه سفر</span> (مانند تفریحی در مقابل تجاری) تغییر می‌کنند.

</template>

<style>
img{
  transform: translateY(25%);
}
.grid-cols-2 {
  column-gap: 20px;
}
</style>

---
dir: rtl
layout: image
---

# وضعیت ساخت آفر در یک نگاه

<img src="./assets/product_offer_matrix.png" height="auto" />


<style>

  img{
    display:block;
    margin:auto;
    height:90%;
  }

</style>

---
layout: section
dir: rtl
---

# فرمول‌سازی مسئله

یک پیشنهاد مجموعه‌ای از محصولات که با یک قیمت واحد به فروش می‌رسند.

---
dir: rtl
---

# یک پیشنهاد چیست

فرض کنید یک ایرلاین $ k $ محصول اتومیک دارد.

---
layout: section
dir: rtl
---

# چگونگی عملکرد MCCM

مزیت MCCM: احتمال خرید باندل‌های غیر سودآور را ضعیف کرده و مشتریان را به خرید پیشنهادات سودآور هدایت می‌کند.

---
layout: center
---

# Results and Performance

we implement a simple model in a hypothetical market wit 2 customer segments to test if our model reaches our desirable result

---
layout: default
---

# Setup
setting assumptions for our experiment

- Airline offers 3 ancillary sevices $\mathcal{A} = \{1,2,3\}$ which are in order bag, seat, and meal
- Customers are equally divided into two segments
  - Leisure travelers
  - Bussiness travelers
- We assume the default parameters are as the ones shown in the next table
- Arrival and transition probabilities are uniform

---
layout: center
---

![](./assets/default_parameters.png)

---
layout: default
---

# Scenarios
what our models look like

**Offer set selection**
- no offer set selection
- unsegmented offer set selection
- segmented offer set selection

**Offer set pricing**
- myopic la carte pricing
- unsegmented pricing
- segmented pricing

---
layout: default
---

# Baseline pricing (myopic)
our base model

3 key assumptions:
- the airline knows the true customer valuation distribution for each ancillary service
- the price for each ancillary is optimized myopically without considering other offers in the offerset
- no bundle discount
the formula for the optimal price for each ancillary service is
$p_a^* = \operatorname{Argmax}_{p_a} \left( 1 - \Phi \left( \frac{p_a - \mu_a}{\sigma_a} \right) \right) (p_a - c_a)$
and the price of each bundle is the sum of included ancillary services' prices $p(0) = \sum_{a \in 0} p_a^*$

Myopic gives a baseline pricing for ailines considering some limitatians they can face

![](./assets/myopic_results.png){style="scale: 0.7;"}

---
layout: default
---

# Full offerset selection, Unsegmented pricing
basic MCCM implemetation

we now implement our MCCM and here the segments are again only diffrent in relevancy
we can observe that the prices are higher on MCCM compared to myopic specially in single ancillary offers in order to insentivise customers to buy bundles at a discount. even tho the total ancillary purchase rate decreases in our model but the expected revenue per customer increases

![](./assets/unsegmccm_results.png){style="scale: 0.8;"}

---
layout: default
---

# Sensitivity analysis
testing how sensitive MCCM is to input parameters

in the table provided in next page we'll see how our result changes based on shifting 3 parameters one at a time each time
- **Cost of provision**: we increase the cost of all 3 ancillaries equally from 0 to 30. the prices increase non linearly in both models and the probability of purchase drops. under more ideal conditions MCCM outperforms myopic by a good margin but under less ideal conditions they have similar results
- **Relevance**: relevance shifts from 10 to 100. since bundle relevance is sirect product of ancillary relevances low relevance means bundles are less attractive but high relevance makes bundles highly attractive
- **Transition probability**: transition probabilty shifts from 0 to 16 percent, so the transition from any offer to no purchase decreases from 100 to 4. as probabilty of no purchase decreases the MCCM becomes alot more profitable
as we can see not only is MCCM scalable and customizable but also bundle prices remain logical and robust

---
layout: center
---

# Sensitivity graphs
sensitivity testing results

![](./assets/sensitivity.png){style="scale: 0.8;"}

---
layout: default
---

# Unsegmented offerset selection, Unsegmented pricing
optimal offerset selection for unsegmented pricing

we systematicaly evaluate all 127 possible $S \subset \Omega$ for each set size |S| we find the S* = $\operatorname{argmax}_S \pi(S, p(S))$, the corresponding price p(s) and the expected purchase rates $\mathcal{P}(S)$ by customer segment.
as we can see the optimal price of an offer changes depending on the offerset unlike myopic this is because MCCM takes into account the risk of no purchase and the potential buy up to a more profitable bundle. we can also see that removing unattractive offers reduces the risk of no purchase
Another thing that we can take into account is the device the customer is using for example a mobile screen may only be able to show up to 3 offers so we have to limit ourselves to |S| $\leq$ 3 

---
layout: center
---

# UU Results
all offerset selection results

![](./assets/unsegprice.png){style="scale: 0.8;"}


---
layout: default
---

# Full/Segmented offerset selction, Segmented pricing

for this scenarios we run 2 seperate MCCM models one for each segment

![](./assets/segmccm_results.png){style="scale: 0.8;"}

---
layout: default
---

# Performance comparison

as we look at the comparison of diffrent scenarios we can see that our model does infact offer an increase to the overall $\pi$*

![](./assets/performance.png){style="scale: 0.8;"}
---
transition: fade
---

<h1 dir="rtl">
منابع
</h1>

- Dynamic offer creation for airline ancillaries using a Markov chain choice model, Kevin K. Wang, 2023


---
layout: end
---
با تشکر از همراهی شما
