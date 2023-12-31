# virtual env
اینvenv به محیط‌ های مجازی در زبان برنامه‌نویسی پایتون اشاره دارد. محیط‌های مجازی یک ابزار قدرتمند در پایتون هستند که به شما اجازه می‌دهند تا بستری جداگانه و مستقل از محیط اصلی سیستم‌عامل برای توسعه و اجرای پروژه‌های پایتون ایجاد کنید.این ویژگی بسیار مفید است زیرا به شما امکان می‌دهد ماژول‌ها، کتابخانه‌ها و وابستگی‌های پروژه‌های مختلف را در محیط‌های مجازی جداگانه نگه دارید و تداخل‌های ممکن در میان آن‌ها را کاهش دهید.

برای ایجاد و مدیریت محیط‌های مجازی در پایتون، شما از دستور `venv` استفاده می‌کنید. در زیر توضیح مراحل ایجاد و استفاده از محیط مجازی با `venv` آمده است:

برای نصب و استفاده از محیط مجازی `venv` در توزیع‌های Debian و CentOS، شما می‌توانید مراحل زیر را دنبال کنید:

## نصب در Debian/Ubuntu:

ابتدا از طریق مدیر بسته‌ها `apt`، پکیج‌های مورد نیاز برای پایتون و محیط مجازی نصب کنید:

   ```
   sudo apt update
   sudo apt install python3 python3-venv
   ```
## نصب در CentOS:

ابتدا از طریق مدیر بسته‌ها `yum`، پکیج‌های مورد نیاز برای پایتون و محیط مجازی نصب کنید:

   ```
   sudo yum install python3 python3-venv
   ```



 **ایجاد محیط مجازی**:
   برای ایجاد محیط مجازی در پوشه‌ای مشخص، از دستور زیر استفاده می‌کنید:
   ```
   python -m venv vnev # دومی مسیر فایل های محیط مجازیمان است
   ```
   در اینجا `myenv` نام موردنظر برای محیط مجازی شماست.

 **فعال‌سازی محیط مجازی**:
   بسته به سیستم‌عامل شما، دستورهای مختلف برای فعال‌سازی محیط مجازی وجود دارد. به طور عمومی، این دستورها به شکل زیر است:
   - در ویندوز:
     ```
     myenv\Scripts\activate
     ```
   - در لینوکس و macOS:
     ```
     source myenv/bin/activate
     ```

 **اجرای دستورات در محیط مجازی**:
   پس از فعال‌سازی محیط مجازی، تمام دستورات پایتونی که اجرا می‌کنید، در محیط مجازی اجرا می‌شوند. همچنین می‌توانید با استفاده از `pip` کتابخانه‌ها و وابستگی‌های موردنیاز پروژه‌تان را نصب کنید.

 **غیرفعال‌سازی محیط مجازی**:
   برای خروج از محیط مجازی و بازگشت به محیط سیستم‌عامل، دستور زیر را وارد می‌کنید:
   ```
   deactivate
   ```

با استفاده از `venv`، شما می‌توانید محیط‌های مجازی مختلفی برای پروژه‌های مختلف ایجاد کرده و به راحتی به آن‌ها جابجا شوید. این کار به بهبود مدیریت و توسعه پروژه‌های پایتون کمک زیادی می‌کند.


## git
برای اینکه محیط مجازیمان نیاز به کامیت در گیت نداشته باشد باید دایرکتوری venv را داخل .gitignore قرار دهیم .


## install a new module on venv
```
# python3 -m venv venv یک محیط مجازی میسازیم
# source venv/bin/activate وارد محیط مجازیمان میشویم

(venv)#  pip freeze  چک میکنیم که پکیجی داخلش نصب نیست
(venv)#  pip install flask  فلاسک را نصب میکنیم


# (venv) pip freeze   چک میکنیم چه پکیج هایی داخل محیط مجازیمان نصب است
blinker==1.6.2
click==8.1.7
Flask==2.3.2
importlib-metadata==6.8.0
itsdangerous==2.1.2
Jinja2==3.1.2
MarkupSafe==2.1.3
werkzeug==2.3.7
zipp==3.16.2

flask --version
Python 3.8.10
Flask 2.3.2
Werkzeug 2.3.7

```
