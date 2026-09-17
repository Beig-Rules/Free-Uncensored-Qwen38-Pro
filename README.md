# Free-Uncensored-Qwen38-Pro

**Advanced free notebook to run Uncensored Qwen3.8-27B models on Google Colab (T4 GPU)**  
**نسخه پیشرفته و رایگان اجرای مدل‌های Uncensored Qwen3.8-27B روی Google Colab**

---

## English Guide – Complete Step-by-Step Tutorial

### What you will get
- A free uncensored Qwen3.8-27B model running on Google’s free T4 GPU
- OpenAI-compatible API + simple Web UI
- Ability to chat with the model from your computer or phone

### Requirements
- A free Google account
- A computer or phone with a browser (Chrome recommended)
- Optional but recommended: a free Hugging Face account + token (for faster download)

---

### Step 1 – Open the notebook

Click this link to open the notebook directly in Google Colab:

**→ [Open Notebook in Colab](https://colab.research.google.com/github/Beig-Rules/Free-Uncensored-Qwen38-Pro/blob/main/Free_Uncensored_Qwen38_Pro.ipynb)**

If the link doesn’t work, go to the repository and click the file `Free_Uncensored_Qwen38_Pro.ipynb` → then click “Open in Colab”.

---

### Step 2 – Enable GPU (very important)

1. At the top menu click **Runtime**
2. Click **Change runtime type**
3. Under “Hardware accelerator” select **T4 GPU**
4. Click **Save**

You must do this before running any cells.

---

### Step 3 – Configure settings (Cell 1)

1. Find the first code cell titled **“۱ - تنظیمات”**
2. Change the password:
   ```python
   PASSWORD = "MyStrongPass123!"
   ```
   Replace it with a strong password of your own.
3. (Optional) Add your Hugging Face token:
   ```python
   HF_TOKEN = "hf_xxxxxxxx"
   ```
   You can create a free token here: https://huggingface.co/settings/tokens
4. Click the **Play** button (▶) on the left of the cell.

---

### Step 4 – Install & Download (Cell 2)

1. Run the second cell (title: “۲ - نصب کامل + دانلود مدل”)
2. This step takes **5 to 15 minutes** the first time.
3. Wait until you see the message:  
   `✅ همه چیز آماده است. حالا سلول ۳ را اجرا کنید.`

Do not close the tab while it is downloading.

---

### Step 5 – Start the server (Cell 3)

1. Run the third cell (title: “۳ - راه‌اندازی SSH + سرور + تونل”)
2. Wait until you see a big success message with a port number.
3. You will receive two important commands:

**SSH command example:**
```bash
ssh -o StrictHostKeyChecking=no -o ServerAliveInterval=30 -p 12345 root@bore.pub
```

**Port-forward command (run this in a second terminal):**
```bash
ssh -N -o StrictHostKeyChecking=no -o ServerAliveInterval=30 -p 12345 -L 3005:127.0.0.1:3005 root@bore.pub
```

Replace `12345` with the port number shown in the notebook.

---

### Step 6 – Connect and use the model

**Option A – Web UI (easiest)**
1. Run the Port-forward command in a terminal and keep it open.
2. Open your browser and go to:  
   **http://localhost:3005**
3. Start chatting with the model.

**Option B – From another app / code**
Use the OpenAI-compatible endpoint:
```
Base URL: http://localhost:3005/v1
API Key: any string (e.g. “local”)
Model: local
```

---

### Step 7 – Keep the session alive

- Keep the Colab browser tab open.
- The notebook has a keep-alive mechanism, but if the session dies, just re-run **Cell 3**.
- Free Colab sessions usually last up to ~12 hours.

---

### Troubleshooting (English)

| Problem | Solution |
|--------|----------|
| No GPU available | Make sure you selected T4 GPU in Runtime settings |
| Download fails | Add a free Hugging Face token in Cell 1 |
| Cannot get bore port | Re-run Cell 3 |
| localhost:3005 not working | Make sure the Port-forward SSH command is still running |
| Session disconnected | Re-run Cell 3 (the port will change) |

---

## راهنمای فارسی – آموزش کامل و قدم‌به‌قدم

### چه چیزی دریافت می‌کنید؟
- مدل Uncensored Qwen3.8-27B به صورت رایگان روی GPU گوگل
- رابط وب ساده + API سازگار با OpenAI
- امکان چت کردن با مدل از کامپیوتر یا موبایل

### پیش‌نیازها
- یک اکانت رایگان گوگل
- مرورگر (ترجیحاً کروم)
- (اختیاری ولی توصیه‌شده) اکانت رایگان Hugging Face + توکن

---

### مرحله ۱ – باز کردن نوت‌بوک

روی لینک زیر کلیک کنید تا نوت‌بوک مستقیماً در Google Colab باز شود:

**→ [باز کردن نوت‌بوک در Colab](https://colab.research.google.com/github/Beig-Rules/Free-Uncensored-Qwen38-Pro/blob/main/Free_Uncensored_Qwen38_Pro.ipynb)**

اگر لینک کار نکرد، به صفحه ریپازیتوری بروید، روی فایل `Free_Uncensored_Qwen38_Pro.ipynb` کلیک کنید و دکمه Open in Colab را بزنید.

---

### مرحله ۲ – فعال کردن GPU (خیلی مهم)

1. از منوی بالای صفحه روی **Runtime** کلیک کنید
2. گزینه **Change runtime type** را انتخاب کنید
3. در قسمت Hardware accelerator گزینه **T4 GPU** را انتخاب کنید
4. روی **Save** کلیک کنید

حتماً این کار را قبل از اجرای هر سلولی انجام دهید.

---

### مرحله ۳ – تنظیمات اولیه (سلول ۱)

1. سلول اول با عنوان **«۱ - تنظیمات»** را پیدا کنید
2. رمز را عوض کنید:
   ```python
   PASSWORD = "MyStrongPass123!"
   ```
   یک رمز قوی به جای آن بنویسید.
3. (اختیاری) توکن Hugging Face را وارد کنید:
   ```python
   HF_TOKEN = "hf_xxxxxxxx"
   ```
   توکن رایگان را از اینجا بسازید: https://huggingface.co/settings/tokens
4. دکمه ▶ کنار سلول را بزنید تا اجرا شود.

---

### مرحله ۴ – نصب و دانلود مدل (سلول ۲)

1. سلول دوم با عنوان **«۲ - نصب کامل + دانلود مدل»** را اجرا کنید
2. این مرحله اولین بار بین **۵ تا ۱۵ دقیقه** طول می‌کشد
3. صبر کنید تا پیام زیر را ببینید:  
   `✅ همه چیز آماده است. حالا سلول ۳ را اجرا کنید.`

تا وقتی دانلود تمام نشده تب را نبندید.

---

### مرحله ۵ – راه‌اندازی سرور (سلول ۳)

1. سلول سوم با عنوان **«۳ - راه‌اندازی SSH + سرور + تونل»** را اجرا کنید
2. صبر کنید تا پیام موفقیت بزرگ همراه با شماره پورت ظاهر شود
3. دو دستور مهم به شما داده می‌شود:

**دستور SSH (مثال):**
```bash
ssh -o StrictHostKeyChecking=no -o ServerAliveInterval=30 -p 12345 root@bore.pub
```

**دستور Forward (در یک ترمینال جداگانه اجرا کنید):**
```bash
ssh -N -o StrictHostKeyChecking=no -o ServerAliveInterval=30 -p 12345 -L 3005:127.0.0.1:3005 root@bore.pub
```

عدد `12345` را با پورتی که نوت‌بوک نشان می‌دهد عوض کنید.

---

### مرحله ۶ – اتصال و استفاده از مدل

**روش آسان (Web UI):**
1. دستور Forward را در ترمینال اجرا کنید و آن را باز نگه دارید
2. مرورگر را باز کنید و به این آدرس بروید:  
   **http://localhost:3005**
3. شروع به چت کردن با مدل کنید

**روش پیشرفته (از طریق کد یا اپلیکیشن):**
```
Base URL: http://localhost:3005/v1
API Key: هر چیزی (مثلاً local)
Model name: local
```

---

### مرحله ۷ – زنده نگه داشتن سشن

- تب مرورگر Colab را باز نگه دارید
- اگر سشن قطع شد، فقط **سلول ۳** را دوباره اجرا کنید (پورت تغییر می‌کند)
- سشن‌های رایگان معمولاً تا حدود ۱۲ ساعت دوام دارند

---

### رفع مشکلات رایج (فارسی)

| مشکل | راه‌حل |
|------|--------|
| GPU در دسترس نیست | مطمئن شوید T4 GPU را در Runtime انتخاب کرده‌اید |
| دانلود مدل شکست می‌خورد | توکن رایگان Hugging Face را در سلول ۱ وارد کنید |
| پورت bore گرفته نمی‌شود | سلول ۳ را دوباره اجرا کنید |
| آدرس localhost:3005 کار نمی‌کند | مطمئن شوید دستور Forward هنوز در حال اجرا است |
| سشن قطع شد | فقط سلول ۳ را دوباره اجرا کنید |

---

## Attribution / اعتبار

This project is inspired by the excellent work of [MorTsaedi/Free-Uncensored-Qwen3.8-27B](https://github.com/MorTsaedi/Free-Uncensored-Qwen3.8-27B).  
این پروژه از کار ارزشمند MorTsaedi الهام گرفته و بهبود یافته است.

---

## License

Code and documentation of this repository are released freely.  
Base models are under Apache 2.0.  
You are fully responsible for how you use uncensored models.

---

**Enjoy your free uncensored Qwen3.8-27B!**  
**از مدل Uncensored خود لذت ببرید!**
