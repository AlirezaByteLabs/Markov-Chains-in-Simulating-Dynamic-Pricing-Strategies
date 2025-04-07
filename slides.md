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
