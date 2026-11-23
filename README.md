<div dir="rtl">

# אוטומציות Make: מטלה 5

שתי אוטומציות ב-Make, עם קובץ Blueprint לכל אחת.

## האוטומציות

**1. חשבוניות מהמייל.** מייל שמועבר לכתובת של Make נבדק בעזרת AI. אם זו חשבונית, ה-AI שולף ממנה ספק, מספר, תאריך, סכום ומטבע, והפרטים נשמרים בטבלה ב-Airtable. מייל שאינו חשבונית נעצר ולא נשמר.

**2. לידים לדשבורד (בונוס 1).** ליד שנשלח ל-webhook מסודר בעזרת AI לפי מקור ותקציב, מקבל את המספר הבא ונציג, ונשמר בטבלה שהדשבורד ממשימה 4 קורא ממנה. ה-webhook מחזיר את מספר הליד שנוצר.

## הקבצים

| קובץ | מה יש בו |
|---|---|
| [blueprints/invoices-from-email.blueprint.json](blueprints/invoices-from-email.blueprint.json) | ה-Blueprint של אוטומציית החשבוניות |
| [blueprints/leads-to-dashboard.blueprint.json](blueprints/leads-to-dashboard.blueprint.json) | ה-Blueprint של אוטומציית הלידים |
| [SPEC.md](SPEC.md) | האפיון המלא של שתי האוטומציות |
| [docs/airtable-setup.md](docs/airtable-setup.md) | הטבלאות והשדות ב-Airtable |
| [docs/tests-invoices.md](docs/tests-invoices.md) | בדיקות אוטומציית החשבוניות |
| [docs/tests-leads.md](docs/tests-leads.md) | בדיקות אוטומציית הלידים |
| [docs/spec-audit.md](docs/spec-audit.md) | בדיקת עמידה באפיון, סעיף אחרי סעיף |

## איך מייבאים Blueprint ל-Make

1. ב-Make נכנסים ל-Scenarios ולוחצים על Create scenario.
2. בעורך לוחצים על שלוש הנקודות בפינה הימנית העליונה ובוחרים Import blueprint.
3. בוחרים את קובץ ה-JSON מהתיקייה blueprints ושומרים.
4. בכל מודול של Airtable בוחרים חיבור Airtable משלכם, ובכל מודול AI בוחרים את Make's AI Provider.
5. במודול הראשון יוצרים webhook או mailhook חדש. הכתובות המקוריות שייכות לחשבון שלי ולא נכללות בקבצים.

## מחקר

- [ההבדל בין Webhook ל-API ומתי להשתמש בכל אחד](https://docs.google.com/document/d/1ugfwrTALa_NhJ5UcIJwZS5Uw4zm0gDSeYPOQzgkCRKk/edit?usp=sharing)
- [שירותים חינמיים ובתשלום לבניית Webhooks](https://docs.google.com/document/d/1o90Bx04hRHsxXVQ0pIoNzusdduorwVGFQjZ9URO6TnM/edit?usp=sharing)

## בונוסים

| בונוס | מצב |
|---|---|
| בונוס 1: אוטומציה לדשבורד | הוגש: אוטומציית הלידים |
| בונוס 2: ייבוא אוטומציה של מישהו אחר | לא הוגש |

</div>
