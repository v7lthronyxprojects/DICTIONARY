# v7lthronyx_DICTIONARY / دیکشنری وی۷ال‌ترونیکس

**v7lthronyx_DICTIONARY** is a powerful password dictionary generator with bilingual support (English/Persian).
**دیکشنری وی۷ال‌ترونیکس** یک ابزار قدرتمند تولید دیکشنری پسورد با پشتیبانی دو زبانه (انگلیسی/فارسی) است.

---

## Features / ویژگی‌ها

- **Personalized Password Generation:** Combines user-specific data such as name, birthdate, phone number, and favorites to generate customized passwords.
- **تولید پسورد شخصی‌سازی شده:** ترکیب داده‌های خاص کاربر مانند نام، تاریخ تولد، شماره تلفن و علاقه‌مندی‌ها برای تولید پسوردهای سفارشی.
  
- **Common Password Datasets:** Utilizes common password lists to enhance password variety.
- **دیتاست‌های پسورد رایج:** استفاده از لیست‌های پسورد رایج برای افزایش تنوع پسوردها.
  
- **Advanced Patterns:** Generates passwords based on various patterns including case variations and number appendages.
- **الگوهای پیشرفته:** تولید پسورد بر اساس الگوهای مختلف از جمله تغییر حالت حروف و اضافه کردن اعداد.
  
- **Machine Learning (Optional):** Uses an MLPClassifier to predict and generate additional passwords based on trained data.
- **یادگیری ماشین (اختیاری):** استفاده از `MLPClassifier` برای پیش‌بینی و تولید پسوردهای اضافی بر اساس داده‌های آموزش دیده.
  
- **Password Strength Evaluation:** Integrates `zxcvbn` to ensure only strong passwords are included.
- **ارزیابی قدرت پسورد:** ادغام `zxcvbn` برای اطمینان از قوی بودن پسوردهای تولید شده.
  
- **Breach Checking:** Checks generated passwords against known breached passwords using the 'Have I Been Pwned' API with k-Anonymity for security.
- **بررسی نفوذ کرده‌ها:** بررسی پسوردهای تولید شده با دیتابیس پسوردهای نفوذ کرده‌ها با استفاده از روش k-Anonymity برای امنیت.
  
- **Progress Indicators:** Utilizes progress bars to provide real-time feedback during lengthy operations.
- **نوار پیشرفت:** استفاده از `tqdm` برای نمایش نوارهای پیشرفت در عملیات طولانی.
  
- **Output Compression:** Optionally compresses the output password list using gzip for efficient storage.
- **فشرده‌سازی خروجی:** امکان فشرده‌سازی فایل خروجی با استفاده از gzip برای ذخیره‌سازی بهینه.
  
- **Logging:** Comprehensive logging to track operations and debug issues.
- **لاگینگ:** ثبت جامع لاگ‌ها برای پیگیری عملیات و اشکال‌زدایی.

- **Sync Datasets:** Optionally sync the datasets before generating passwords.
- **همگام‌سازی دیتاست‌ها:** امکان همگام‌سازی دیتاست‌ها قبل از تولید رمز عبور.

---

## Installation / نصب

1. Clone the Repository / کلون کردن مخزن:

   ```bash
   git clone https://github.com/v7lthronyxprojects/DICTIONARY.git
   cd DICTIONARY
pip install -r requirements.txt

python main.py --datasets wordlist.txt --output passwords.txt

python main.py --datasets wordlist1.txt wordlist2.txt \
               --user-data "John,1990-01-01,1234567890" \
               --output generated_passwords.txt \
               --compress \
               --use-ml \
               --check-breach \
               --sync


                              # Sync all datasets / همگام‌سازی تمام دیتاست‌ها
               python main.py --sync
               
               # Sync and generate passwords / همگام‌سازی و تولید پسورد
               python main.py --sync --datasets common_passwords.txt
