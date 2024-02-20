# نصب و راه‌اندازی

در این آموزش، می‌خواهیم AlienVault OSSIM را با استفاده از VMware Workstation Pro راه اندازی کنیم.

## ساخت و پیکربندی ماشین مجازی

ابتدا فایل `AlienVault_OSSIM_64bits.iso` را از [OSSIM Download](https://cybersecurity.att.com/products/ossim/download) دانلود کنید.

1. VMware را اجرا کنید و `Create a New Virtual Machine` را بزنید.  

![vmware1](assets/vmware1.png){: style="height:480px"}  
2. `Typical` را انتخاب کرده و `Next` را بزنید.

![vmware1](assets/vmware2.png){: style="height:480px"}  
3. فایل `AlienVault_OSSIM_64bits.iso` را انتخاب کرده و `Next` را بزنید.  

![vmware1](assets/vmware3.png){: style="height:480px"}  
4. نام و محل ذخیره ماشین مجازی را مشخص کنید و `Next` را بزنید. توجه کنید که در محل ذخیره انتخاب شده حداقل `50` گیگابایت فضای خالی وجود داشته باشد.  
![vmware1](assets/vmware4.png){: style="height:480px"}  
5. در اینجا `Maximum Disk Size` را بر روی `50` گیگابایت قرار داده و `Next` را بزنید.  

![vmware1](assets/vmware5.png){: style="height:480px"}  
6. در این صفحه `Customize Hardware` را انتخاب کنید.  

![vmware1](assets/vmware6.png){: style="height:480px"}  
7. `Memory` را حداقل بر روی `4` گیگابایت قرار دهید.  

![vmware1](assets/vmware7.png){: style="height:480px"}  
8. `Number of cores per processor` را حداقل بر روی `2` هسته قرار دهید.  

![vmware1](assets/vmware8.png){: style="height:480px"}  
9. در پایین صفحه بر روی `...Add` کلیک کنید و یک `Network Adapter` اضافه کنید.  

![vmware1](assets/vmware9.png){: style="height:480px"}  
10. در تنظیمات `Network Adapter 2` نوع آن را بر روی `Host-only` قرار دهید.  

![vmware1](assets/vmware10.png){: style="height:480px"}  
11. `Close` و سپس `Finish` را بزنید و صبر کنید تا ماشین مجازی اجرا شود.  

## نصب OSSIM

اکنون که ماشین مجازی ساخته شده و پیکربندی آن هم انجام شده به سراغ اصل کار یعنی نصب OSSIM و پیکربندی آن در داخل ماشین مجازی می‌رویم.

1. پس از بالا آمدن ماشین مجازی، با صفحه زیر روبرو خواهید شد. گزینه اول یعنی Install AlienVault OSSIM را انتخاب کنید و با زدن کلید Enter به مرحله بعد بروید.  

![ossim1](assets/OSSIM1.png){: style="height:480px"}  
2. تنظیمات زبان، منطقه و کیبورد را انجام دهید.  

![ossim2](assets/OSSIM2.png){: style="height:480px"}
![ossim3](assets/OSSIM3.png){: style="height:480px"}
![ossim4](assets/OSSIM4.png){: style="height:480px"}  
3. در اینجا باید کارت شبکه مجازی NAT که در تنظیمات VMware مشخص کردید را انتخاب کنید. اگر مطابق این آموزش جلو آمده باشید، اولین کارت شبکه که بر روی اینترفیس eth0 قرار دارد همان کارت شبکه NAT است. آن را انتخاب کنید و به مرحله بعد بروید.  

![ossim5](assets/OSSIM5.png){: style="height:480px"}  
برای دیدن تنظیمات مربوط به کارت شبکه IP آنها، از منوی بالای VMware  وارد Edit و سپس Virtual Network Editor شوید.  

![vmware11](assets/vmware11.png){: style="height:480px"}
![vmware12](assets/vmware12.png){: style="height:480px"}  
4. IP اینترفیس NAT را وارد کنید. در اینجا این IP برای ما 192.168.88.1 است.  

![ossim6](assets/OSSIM6.png){: style="height:480px"}  
5. netmask را وارد کنید.  

![ossim7](assets/OSSIM7.png){: style="height:480px"}  
6. IP Gateway را وارد کنید. Gateway اینترفیس NAT برای ما مطابق با تنظیمات VMware برابر 192.168.88.2 است.  

![ossim8](assets/OSSIM8.png){: style="height:480px"}  
7. در اینجا باید آدرس DNS را وارد کنید. میتوانید تا 3 آدرس DNS که با یک فاصله از هم جدا شده اند را وارد کنید. ما 192.168.88.2 و 8.8.8.8 را وارد می‌کنیم.  

![ossim9](assets/OSSIM9.png){: style="height:480px"}  
8. یک رمز عبور برای کاربر root انتخاب کنید و به مرحله بعد بروید.  

![ossim10](assets/OSSIM10.png){: style="height:480px"}  
9. منطقه زمانی را انتخاب کنید. ما Eastern را انتخاب می‌کنیم.  

![ossim12](assets/OSSIM12.png){: style="height:480px"}  
10. صبر کنید تا عملیات نصب انجام شود. این مرحله بسته به قدرت سخت افزاری شما ممکن است از 15 الی 45 دقیقه به طول انجامد.  

![ossim13](assets/OSSIM13.png){: style="height:480px"}
![ossim14](assets/OSSIM14.png){: style="height:480px"}
![ossim15](assets/OSSIM15.png){: style="height:480px"}  
11. پس از اتمام نصب با صفحه زیر روبرو خواهید شد. نام کاربری root و رمز عبوری که در مرحله 8 ایجاد کردید را وارد کرده و لاگین کنید.  

![ossim16](assets/OSSIM16.png){: style="height:480px"}  
12. پس از ورود به صفحه تنظیمات باید آدرس Web UI را تنظیم کنیم. همانطور که گفتیم از آنجا که آدرس 192.168.88.1 مربوط به اینترفیس NAT هست، نمیتوان با آن از طریق مرورگر به صفحه تحت وب OSSIM وارد شد و باید اینترفیس دیگری را به این کار اختصاص دهیم. ما از اینترفیس Host-Only که در ابتدای کار در تنظیمات VMware ایجاد کردیم برای این کار استفاده می‌کنیم.  
13. به ترتیب وارد System Preferences > Configure Network > Setup Management Network شده و با استفاده از کلید Space، اینترفیس eth1 که مربوط به کارت شبکه Host-Only است را انتخاب کرده و با زدن Enter وارد تنظیمات آن شوید.  

![ossim17](assets/OSSIM17.png){: style="height:480px"}
![ossim18](assets/OSSIM18.png){: style="height:480px"}
![ossim19](assets/OSSIM19.png){: style="height:480px"}
![ossim20](assets/OSSIM20.png){: style="height:480px"}  
14. در اینجا باید یک IP در رنج IP اینترفیس Host-Only که برای ورود به صفحه تحت وب OSSIM استفاده می‌شود را وارد کنید. آدرس IP اینترفیس Host-Only در تنظیمات VMware برای ما 192.168.58.1 است که ما آی پی 192.168.58.10 را برای Web UI انتخاب می‌کنیم.  

![ossim21](assets/OSSIM21.png){: style="height:480px"}  
15. netmask متناسب را وارد کنید. در اینجا ما 255.255.255.0 را وارد می‌کنیم.  

![ossim22](assets/OSSIM22.png){: style="height:480px"}  
16. Gateway را بر روی آدرس Gateway اینترفیس NAT قرار دهید. این آدرس برای ما 192.168.88.2 است.  

![ossim23](assets/OSSIM23.png){: style="height:480px"}  
17. با زدن Back به صفحه اول تنظیمات برگشته و گزینه آخر یعنی Apply all Changes را بزنید تا تنظیمات اعمال شوند.  

![ossim24](assets/OSSIM24.png){: style="height:480px"}
![ossim25](assets/OSSIM25.png){: style="height:480px"}  
18. پس از اعمال تنظیمات، با استفاده از آدرسی که در مرحله 14 انتخاب کردید وارد صفحه تحت وب OSSIM شوید. این آدرس برای ما https://192.168.58.10 است. در اولین ورود باید نام، رمز عبور و ایمیل موردنظر را برای کاربر Admin به منظور ورود به کنسول مدیریت تحت وب OSSIM تعریف کنید. پس از آن می‌توانید با نام کاربری Admin و رمزعبور انتخاب شده، وارد کنسول تحت وب OSSIM شوید.

![WebUI](assets/WebUI.png){: style="height:480px"}
![WebUI](assets/WebUI2.png){: style="height:480px"}
![WebUI](assets/WebUI3.png){: style="height:480px"}
