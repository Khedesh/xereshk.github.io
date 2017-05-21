## به نام خداوند بخشنده مهربان

### Python MRO
#### توضیحات کلی
در پایتون الگوریتم
MRO 
 یا 
(Method Resolution Order)
مسیر جست و جوی کلاس‌ها برای یافتن تابع درست به منظور به کارگیری در هنگام صدازدن تابع کلاس‌ها در ارث‌بری چندگانه را تعیین می‌کند.

این الگوریتم در پایتون ۲.۲ به ۲.۳ تغییراتی کرده است و به منظور نگهداری سازگاری برای استفاده از آن در پایتون ۲.۳ به بعد می بایست تا از کلاس
object 
ارث‌بری انجام شود. اما در پایتون ۳ به طور پیش‌فرض از الگوریتم جدید استفاده می‌شود.

برای مثال در کد زیر مسیری که
MRO 
تعیین می کند با استفاده از الگوریتم قدیمی
است.

```markdown

class A :
    pass
class B :
    pass
class C(A, B) :
    pass
    
```
اما اگر در پایتون ۲.۳ به بعد به صورت زیر به کار رود از الگوریتم جدید استفاده می‌کند:
```markdown
class A(object) :
    pass
class B(object) :
    pass
```

#### توضیح الگوریتم قدیمی
با مثال زیر آغاز می‌کنیم:
```markdown
class A:
    def who_am_i(self):
        print("I am a A")

class B(A):
    def who_am_i(self):
        print("I am a B")

class C(A):
    def who_am_i(self):
        print("I am a C")

class D(B,C):
    def who_am_i(self):
        print("I am a D")

d1 = D()
d1.who_am_i()
```
پس از اجرای کد بالا در پایتون ۲ خواهیم داشت:

```markdown
$ python2 Python-MRO.py  
I am a D
```
پس از کامنت‌کردن کد 
D خواهیم داشت:

```markdown
class D(B,C):
\#    def who_am_i(self):
\#        print("I am a D")
    pass
```

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Khedesh/xereshk.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
