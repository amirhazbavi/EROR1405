<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6c5ce7,50:1e293b,100:0f172a&height=280&section=header&text=همه‌ی%20مدل‌های%20خطا&fontSize=46&fontColor=ffffff&animation=fadeIn&fontAlignY=32&desc=یه%20راهنمای%20جدی%20برای%20خطاهای%20کاملاً%20غیرجدی&descAlignY=54&descSize=18" width="100%" alt="header" />

<img src="https://http.cat/418" width="320" alt="I'm a teapot" />

<br/>

> **«من یک قوری هستم.»**
> — اولین مواجهه‌ی مستند بشر با یک مدل خطای طنز، HTTP 418، سال ۱۹۹۸

<img src="https://readme-typing-svg.demolab.com?font=Vazirmatn&weight=700&size=22&pause=900&color=6C5CE7&center=true&vCenter=true&width=900&lines=خطا+حتماً+اتفاق+می‌افتد;سؤال+این+است+که+چه+مدلی+برای+آن+داری؟;Fault+%E2%86%92+Error+%E2%86%92+Failure" alt="typing" />

<br/>

<img src="https://img.shields.io/badge/نسخه-3.0-6c5ce7?style=for-the-badge&logo=semver&logoColor=white" alt="version" />
<img src="https://img.shields.io/badge/وضعیت-کامل-2ea44f?style=for-the-badge&logo=checkmarx&logoColor=white" alt="status" />
<img src="https://img.shields.io/badge/حال%20و%20روز-خوب-ff69b4?style=for-the-badge&logo=icloud&logoColor=white" alt="mood" />
<img src="https://img.shields.io/badge/قوری-418-ffb703?style=for-the-badge&logo=buymeacoffee&logoColor=white" alt="teapot" />

<br/><br/>

<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%" alt="divider" />

</div>

---

<div align="center">

## فهرست مطالب

| مقدمه | زنجیره خطا | طبقه‌بندی | سخت‌افزار | نرم‌افزار | شبکه | امنیت | انسان | عملیات | جمع‌بندی |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| [مقدمه](#مقدمه) | [زنجیره](#زنجیرهی-خطا-fault--error--failure) | [طبقه‌بندی](#طبقهبندی-خطاها) | [HW](#مدلهای-خطای-سختافزاری) | [SW](#مدلهای-خطای-نرمافزاری) | [شبکه](#مدلهای-خطای-شبکه-و-توزیعشده) | [امنیت](#مدلهای-خطای-امنیتی) | [انسان](#مدلهای-خطای-انسانی) | [عملیات](#مدلهای-عملیاتی-و-آماری) | [جمع‌بندی](#جمعبندی) |

</div>

---

<div align="center">
<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%" alt="divider" />
</div>

## مقدمه

هیچ نرم‌افزاری بدون خطا نیست؛ همان‌قدر که هیچ برنامه‌نویسی بدون قهوه کد نمی‌زند. **مدل خطا** یک قاب انتزاعی است که می‌گوید «چه نوع خرابی‌هایی ممکن است رخ دهد و چگونه باید در طراحی و تست لحاظ شوند». انتخاب مدل خطا = انتخاب سطح پذیرش ریسک.

> **قانون طلایی:** اگر مدل خطایت را نشناسی، خطا تو را می‌شناسد.

## زنجیره‌ی خطا: Fault → Error → Failure

| مرحله | تعریف | مثال |
|:---|:---|:---|
| **Fault** | نقص ایستا در کد یا طراحی | یک شرط مرزی اشتباه در حلقه |
| **Error** | وضعیت نادرست درونی هنگام اجرا | مقدار شمارنده منفی می‌شود |
| **Failure** | رفتار نادرست قابل مشاهده از بیرون | سرویس کرش می‌کند |

مثال روزمره: چای‌ریز قوری (Fault) → قوری نمی‌جوشد (Error) → صبحت خراب می‌شود (Failure).

## طبقه‌بندی خطاها

<table align="center">
<tr>
<td align="center" width="33%">

<img src="https://img.shields.io/badge/زمان-گذرا%20%7C%20ماندگار-6c5ce7?style=for-the-badge" alt="time" />

**بر اساس زمان:** گذرا، متناوب، ماندگار.

</td>
<td align="center" width="33%">

<img src="https://img.shields.io/badge/منشأ-انسانی%20%7C%20محیطی-2ea44f?style=for-the-badge" alt="origin" />

**بر اساس منشأ:** انسانی، سخت‌افزاری، محیطی، طراحی.

</td>
<td align="center" width="33%">

<img src="https://img.shields.io/badge/شدت-کشنده%20%7C%20جزئی-e74c3c?style=for-the-badge" alt="severity" />

**بر اساس شدت:** کشنده، بحرانی، جزئی، آرایشی.

</td>
</tr>
</table>

## مدل‌های خطای سخت‌افزاری

- **Stuck-at (گیرکرده در ۰ یا ۱):** ساده‌ترین و پرکاربردترین مدل تست مدارهای دیجیتال.
- **Bridging (پل‌شدن):** اتصال ناخواسته دو مسیر.
- **Transition Delay:** کندی در گذار بین دو وضعیت.
- **Bit-flip:** تغییر ناگهانی بیت، به‌ویژه در حافظه (رویداد SEU کیهانی!).
- **Erasure / Silent Corruption:** داده گم می‌شود یا بی‌صدا خراب می‌شود.

## مدل‌های خطای نرم‌افزاری

مدل‌های آماری قابلیت اطمینان که روی داده‌ی «زمان بین خرابی» (TBF) کار می‌کنند:

| مدل | ایده اصلی | فرض کلیدی |
|:---|:---|:---|
| **Jelinski–Moranda** | نرخ خرابی متناسب با تعداد خطاهای باقیمانده | خطاها مستقل و هم‌احتمال |
| **Goel–Okumoto** | نرخ خرابی نمایی نزولی | اصلاح خطا در طول زمان |
| **Musa** | مدل اجرایی، مبتنی بر زمان CPU | تخمین دقیق‌تر در محصول |
| **Littlewood–Verall** | نرخ خرابی کاهش تدریجی | خطاهای هم‌وزن نیستند |
| **S-shaped** | نرخ صعودی سپس نزولی | فاز یادگیری |

## مدل‌های خطای شبکه و توزیع‌شده

- **Crash:** نود بی‌صدا متوقف می‌شود.
- **Crash-Recover:** توقف و بازگشت با حالت ناشناخته.
- **Omission:** پیام ارسال یا دریافت نمی‌شود.
- **Timing:** پیام دیر می‌رسد (دنیای ناهمگام).
- **Byzantine (بیزانسی):** نود دروغ می‌گوید؛ بدترین حالت ممکن.
- **Partition:** شبکه به دو جزیره تقسیم می‌شود.

> اگر مدل خطای Byzantine را برای اولین بار می‌خوانی، خیالت راحت باشد — هنوز هم بامزه است.

## مدل‌های خطای امنیتی

- **STRIDE:** Spoofing، Tampering، Repudiation، Information Disclosure، DoS، Elevation of Privilege.
- **CWE / CVE:** تاکسونومی آسیب‌پذیری‌ها.
- **Threat Modeling (PASTA, OCTAVE):** شناسایی تهدید پیش از کد.
- **Attack Tree:** درخت حمله برای مرزبندی سناریوها.

## مدل‌های خطای انسانی

- **Swiss Cheese Model (Reason):** چند لایه دفاعی، هر لایه سوراخ دارد؛ فاجعه وقتی رخ می‌دهد که سوراخ‌ها هم‌راستا شوند.
- **Human Error Taxonomy:** Slip، Lapse، Mistake، Violation.
- **Just Culture:** خطای سیستمی در برابر خطای فردی.

## مدل‌های عملیاتی و آماری

| سنجه | معنا |
|:---|:---|
| **MTBF** | میانگین زمان بین خرابی‌ها |
| **MTTF** | میانگین زمان تا اولین خرابی |
| **MTTR** | میانگین زمان بازیابی |
| **Availability** | MTTF / (MTTF + MTTR) |
| **Error Budget** | بودجه خطای مجاز در SRE |

## جمع‌بندی

هر مدل خطا یک **لنز** است؛ هیچ لنزی کل واقعیت را نمی‌بیند. مدل را بر اساس ریسک انتخاب کن، نه بر اساس مُد روز. و یادت باشد: اگر همه‌چیز خوب پیش می‌رود، احتمالاً یک قوری ۴۱۸ جایی منتظر توست.

---

<div align="center">

<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="100%" alt="divider" />

<img src="https://http.cat/500" width="180" alt="500" />
<img src="https://http.cat/404" width="180" alt="404" />
<img src="https://http.cat/418" width="180" alt="418" />

<br/>

<img src="https://img.shields.io/badge/اصل%20طلایی-مدل%20خطا%20را%20انتخاب%20کن-6c5ce7?style=for-the-badge" alt="golden" />
<img src="https://img.shields.io/badge/هیچ%20خطایی-بی‌مدل%20نیست-2ea44f?style=for-the-badge" alt="no-error" />
<img src="https://img.shields.io/badge/قوری-همیشه%20بیدار-ffb703?style=for-the-badge" alt="teapot" />

<br/><br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:ffb703,50:6c5ce7,100:0f172a&height=170&section=footer&text=همه‌ی%20مدل‌های%20خطا%20—%20v3.0&fontSize=22&fontColor=ffffff&animation=fadeIn&fontAlignY=65" width="100%" alt="footer" />

</div>
