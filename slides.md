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

# ساخت و قیمت گذاری آفر در یک نگاه

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

یک پیشنهاد ۲ بخش دارد مجمو‌عه‌ای ناتهی از محصولات و یک قیمت .

---
dir: rtl
---

# یک پیشنهاد چیست
<br>

فرض کنید یک ایرلاین 
$k$ 
محصول اتومیک دارد.

<div dir="ltr">

$$A = \{1,2, \cdots , k\}$$

$$a=1,\dots ,K$$

$$O\subseteq \mathcal{A}$$

$$\Omega =\mathrm{P}\left(\mathcal{A}\right)\backslash \left\{ \emptyset \right\}$$

$$\left|\Omega \right|={2}^{K}-1$$

</div>

---
dir: rtl
---

# مجموعه پیشنهاد قیمت گذاری نشده چیست

<br>

<div dir="ltr">

$$S=\left\{ {O}_{1},\dots ,{O}_{N}\right\}$$

$$S\subseteq\Omega$$

$$1\le N\le |\Omega |$$

$$\mathrm{P}\left(\Omega \right)\backslash \left\{ \emptyset \right\}$$

$${O}_{0}=\emptyset$$

$$S\cup \left\{ {O}_{0}\right\}=\left\{ {O}_{0},{O}_{1},\dots ,{O}_{N}\right\}$$

</div>

---
dir: rtl
---

# مجموعه پیشنهاد قسمت گذاری شده

<br>

فرض کنید $S$ یک مجموعه پیشنهاد قیمت گذاری نشده باشد.

<div dir="ltr">

$$ {\mathbf{p}}\left(S\right)=\left({p}_{1}(S),\dots ,{p}_{N}(S) \right) $$

$${p}_{i}\left(S\right)={p}_{i}={ {p}_{O_{i}}}$$

$${p}_{0}(S)=0$$

</div>

---
dir: rtl
---

# یک مثال

<div dir="ltr">

$$K=3$$

$$\mathcal{A}=\left\{\mathrm{1,2},3\right\}$$

$$\Omega =\mathrm{P}\left(\mathcal{A}\right)\backslash \left\{ \emptyset \right\}$$

$$\left|\Omega \right|=7$$

$$\Omega =\left\{ {O}_{1},{O}_{2},{O}_{3},{O}_{4},{O}_{5},{O}_{6},{O}_{7}\right\}=\left\{\left\{1\right\}, \left\{2\right\}, \left\{3\right\},\left\{\mathrm{1,2}\right\},\left\{\mathrm{1,3}\right\}, \left\{\mathrm{2,3}\right\}, \left\{\mathrm{1,2},3\right\}\right\}$$

$${S}_{1}=\left\{\left\{1\right\}, \left\{2\right\}, \left\{\mathrm{1,2},3\right\}\right\}$$

$${S}_{2}= \left\{\left\{1\right\}, \left\{3\right\},\left\{\mathrm{1,2},3\right\}\right\}$$

$$S=\Omega \text{ , S isfull offer set}$$

</div>

---
dir: rtl
---

# تعریف تابع هدف بهینه سازی

<br>

### یک فرض مهم
فرض می‌کنیم مشتری فقط یک پیشنهاد را برای خرید انتخاب می‌کند


<div dir="ltr">

$$\left\{\left\{1\right\},\left\{2\right\}\right\} \implies \left\{\left\{1\right\},\left\{2\right\},\{\mathrm{1,2}\}\right\}$$

</div>

### مدل انتخاب گسسته

<div dir="ltr">

$$\mathcal{P}\left({O}_{i}|S,{\mathbf{p}}\left(S\right)\right)$$

</div>

این تابع مشخص کننده احتمال خرید محصول 
<span dir="ltr">
${O}_{i}$
</span>
در بین 
<span dir="ltr">
$S=\left\{ {O}_{1},\dots ,{O}_{N}\right\}$
</span>

### تابع هدف درامد مورد انتظار

<div dir="ltr">

$$\begin{array}{c}\pi \left(S, {\mathbf{p}}\left(S\right)\right)=\sum\limits_{i=1}^{N}\left({p}_{i}-{c}_{i}\right)\mathcal{P}\left({O}_{i}|S, {\mathbf{p}}\left(S\right)\right)\end{array}$$

</div>

---
dir: rtl
---

# مقدار تابع احتمال خرید پیشنهاد

<br>

احتمال خرید یک پیشنهاد از مجموع پیشنهادات برابر تعداد دفعاتی است که آن محصول دیده‌می‌شود.

<div dir="ltr">

$$\mathcal{P}(O_i|S, \bm{p}(S)) = v_i(\bm{p}(S)) \theta_i(p_i)$$

</div>

<br>

که با توجه به پارامتر‌های تایین می‌توان مقدار $v_i$ را تعیین نمود.

<div dir="ltr">

$$v_i(\bm{p}(S)) = \lambda_i + \sum_{j=1,\dots,N} \rho_{ji} (1 - \theta_j(p_j)) v_j(\bm{p}(S))$$

</div>

---
dir: rtl
---

# بهینه سازی روی تابع هدف

<br>

<div dir="ltr">

$$\begin{array}{c}\pi \left(S, {\mathbf{p}}\left(S\right)\right)=\sum\limits_{i=1}^{N}\left({p}_{i}-{c}_{i}\right)\mathcal{P}\left({O}_{i}|S, {\mathbf{p}}\left(S\right)\right)\end{array}$$

</div>

### بهینه سازی این تابع به ۲ عامل بستگی دارد:
<br>

#### قیمت اعلام شده برای پیشنهاد
ورودی: $S$ یک مجموعه بدون قیمت است.
<div dir="ltr">

$${ {\mathbf{p} } }^{\boldsymbol{*} }\left(S\right)={\mathrm{argmax} }_{ {\mathbf{p} } }\pi \left(S,{\mathbf{p} }\left(S\right)\right)$$

</div>


#### انتخاب مجموعه پیشنهادها
ورودی: <span dir="ltr"> ${\mathbf{p}}\left(S\right)$, $S\subseteq\Omega$ </span>

<div dir="ltr">

$$S^*={\mathrm{argmax} }_{S\subseteq \Omega }\pi \left(S,{\mathbf{p} }\left(S\right)\right)$$

</div>

---
dir: rtl
layout: fact
---

مسئله‌ قیمت‌گذاری و انتخاب مجموعه پیشنهادها به <span v-mark.red="0">صورت ترکیبی</span>، پیچیدگی جدیدی ایجاد نمی‌کند و این ۲ مسئله را به صورت جست و جوی جامع حل می‌کنیم. به عبارت دیگر برای همه مجموعه پیشنها‌های ممکن به دنبال قیمت بهینه می‌گردیم و مواردی را انتخاب می‌کنیم که بهتر سود را داشته باشد.


---
dir: rtl
---

# ویژگی‌های مهم


- ویژگی‌های مدل انتخاب گسسته <span dir="ltr"> $\mathcal{P}\left({O}_{i}|S, {\mathbf{p}}\left(S\right)\right)$ </span>

  - **مقیاس‌پذیر:**  
    احتمالات خرید حتی برای مجموعه‌های پیشنهادی بزرگ نیز قابل محاسبه هستند.

  - **قابل سفارشی‌سازی:**  
    مجموعه پیشنهادها را می‌توان متناسب با هر مشتری تنظیم کرد.

  - **قابل تفسیر:**  
    یک مدل پارامتری انتخاب گسسته که امکان تفسیر نتایج را فراهم می‌کند.

  - **قابل برآورد:**  
    پارامترهای مدل را می‌توان از داده‌های آموزشی تخمین زد.

  - **قابل مدیریت:**  
    حتی برای مجموعه‌های پیشنهادی بزرگ، می‌توان قیمت‌های بهینه برای حداکثر سود یا بهترین مجموعه پیشنهادی را به راحتی تعیین کرد.


---
dir: rtl
---

# ویژگی‌های مهم


- قیمت منطقی

<div dir="ltr">

$$S = \left\{\left\{1\right\},\left\{2\right\},\{\mathrm{1,2}\}\right\}$$

$$\mathrm{max}({p}_{\left\{1\right\}},{p}_{\left\{2\right\}}) \le {p}_{\left\{\mathrm{1,2}\right\}} \le {p}_{\left\{1\right\}}+{p}_{\left\{2\right\}}$$

</div>


---
layout: section
dir: rtl
---

# چگونگی عملکرد MCCM

مزیت MCCM: احتمال خرید باندل‌های غیر سودآور را ضعیف کرده و مشتریان را به خرید پیشنهادات سودآور هدایت می‌کند.

---
dir: rtl
---

# شیوه عملکرد زنجیر‌های مارکوفی

<img src="./assets/markov_chain.png" style="height: 85%; width: auto; margin:auto;"/>

---
dir: rtl
---

# بهینه‌کردن قیمت
به کمک فراید تصمیم گیری مارکوفی

## مفاهیم مورد نیاز

<br>

تعریف فرمال یک مسئله بهینه سازی
<div dir="ltr">

$$\left(\mathcal{S},\mathcal{A},\mathcal{R},\mathcal{P}\right)$$

</div>

- مجموعه حالات ممکن <span dir="ltr"> $\mathcal{S}=S\cup \{ {O}_{0},T\}$, $S=\left\{ {O}_{1},\dots ,{O}_{N}\right\}\subseteq\Omega$ </span> 
- مجموعه قیمت‌های ممکن <span dir="ltr"> $\mathcal{A}={\mathbb{R} }_{+}$</span> 
-  درامد حاصل <span dir="ltr"> $\mathcal{R}(O_i,p_i,s') = (p_i-c_i)\cdot\mathbb{I}_{s'=T}$ </span>
- احتمال رفتن از s به 's
    <span dir="ltr"> $\mathcal{P}(O_i, p_i, s') = 
\begin{cases} 
\theta_i(p_i) & \text{if } s' = T \\
(1 - \theta_i(p_i)) \rho_{ij} & \text{if } s' = O_j \\
(1 - \theta_i(p_i))(1 - \sum_{j>0} \rho_{ij}) & \text{if } s' = O_0 
\end{cases}$ </span> 
---
dir: rtl
---

# بهینه‌کردن قیمت
به کمک فراید تصمیم گیری مارکوفی

## تابع هدف بهینه سازی

<div dir="ltr">

$$V^*(s) = \max_{\bm{p}} \sum_{s' \in \mathcal{S}} \mathcal{P}(s, \bm{p}, s') \big[ \mathcal{R}(s, \bm{p}, s') + V^*(s') \big]$$

</div>

که <span dir="ltr">$V^*(s)$</span> نشان دهنده درامد بهینه است.

<br>

که این تابع دارای شرایط تابع بلمن است که به صورت زیر حل می‌شود.


<div dir="ltr">

$$V_{k+1}(s) = \max_{\bm{p}} \sum_{s' \in \mathcal{S}} \mathcal{P}(s, \bm{p}, s') \left[ \mathcal{R}(s, \bm{p}, s') + V_k(s') \right]$$

</div>

با توجه به داشتن شرایط تابع بلمن این تابع با هر حدس اولیه‌ای همگرا خواهد بود. (مبلغ آغازین مهم نیست)


---
dir: ltr
layout: fact
---


$$\bm{p}^*(s) = \arg\max_{\bm{p}} V^*(s)$$

---
dir: rtl
---

# افراز مشتریان

برای اینکه بتوانیم با توجه به موضوع سفر پیشنهادات مناسب ارايه دهیم مشتریان را به l دسته افراز می‌کنیم.

<div dir="ltr">

$$\theta_{i,l}(p) = \left( \prod_{a \in O_i} \phi_{a,l} \right) \left( 1 - \Phi \left( \frac{p_i - \mu_{O_i,l}}{\sigma_{O_i,l}} \right) \right)$$

$$\theta_{i}(p_i) = \sum_{l=1}^{L} w_l \theta_{i,l}(p_i)$$

</div>

- که در آن Φ(𝑥) تابع توزیع تجمعی (CDF) متغیر نرمال استاندارد 𝑁(0,1) است.
- <span dir="ltr">$\phi_{a,l}$</span> نشان دهده ارتباط خدمات جانبی $i$ به افراز $l$ام است.


---
layout: center
---

# Results and Performance

we implement a simple model in a hypothetical market wit 2 customer segments to test if our model reaches our desirable result

---
layout: section
---

# Sections

- Setup
- Scenarios
- Baseline pricing 
- Full offerset selection, Unsegmented pricing
- Sensitivity analysis
- Unsegmented offerset selection, Unsegmented pricing
- Full/Segmented offerset selction, Segmented pricing
- Performance comparison

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
