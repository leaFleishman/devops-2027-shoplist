
# בחירת Image בסיס של Python עם גרסה מדויקת, ללא latest
FROM python:3.12.12-slim

# הגדרת תיקיית העבודה בתוך ה-Container
WORKDIR /app

# העתקת קובץ התלויות לפני העתקת הקוד כדי לאפשר שימוש ב-Cache
COPY requirements.txt .

# התקנת התלויות הדרושות לאפליקציה
RUN pip install --no-cache-dir -r requirements.txt

# העתקת קובצי האפליקציה לתוך ה-Container
COPY app.py .

# הצהרה שהאפליקציה מאזינה בפורט 8000
EXPOSE 8000

# הגדרת הפקודה להפעלת האפליקציה בצורת exec
CMD ["python", "app.py"]
