<div dir="rtl">

# אוטומציות Make: מטלה 5

בניתי ב-Make שתי אוטומציות, ייבאתי אוטומציה שלישית מתבנית ציבורית, וייצאתי כל אחת מהן לקובץ Blueprint.

**1. חשבוניות מהמייל.** אני מעביר מייל לכתובת mailhook של Make. שלב AI בודק אם המייל הוא חשבונית. אם כן, שלב AI שני שולף ממנה ספק, מספר, תאריך, סכום ומטבע, והפרטים נשמרים בטבלה ב-Airtable. מייל שאינו חשבונית נעצר ולא נשמר.

**2. לידים לדשבורד (בונוס 1).** ליד שנשלח ל-webhook מסודר בעזרת AI לפי מקור ותקציב, מקבל את המספר הבא ונציג, ונשמר בטבלת הלידים ב-Airtable שהדשבורד שלי ממטלה 4 קורא ממנה. ה-webhook מחזיר את מספר הליד שנוצר.

**3. ציון לידים עם Claude (בונוס 2).** ייבאתי ל-Make תבנית ציבורית שמישהו אחר בנה, וחיברתי אותה לטבלת הלידים. Claude קורא ליד, נותן לו ציון וסיכום קצר, והם נשמרים בליד. הפרטים ב-[docs/bonus2-claude-template.md](docs/bonus2-claude-template.md).

## הקבצים

| קובץ | מה יש בו |
|---|---|
| [blueprints/invoices-from-email.blueprint.json](blueprints/invoices-from-email.blueprint.json) | ה-Blueprint של אוטומציית החשבוניות |
| [blueprints/leads-to-dashboard.blueprint.json](blueprints/leads-to-dashboard.blueprint.json) | ה-Blueprint של אוטומציית הלידים |
| [blueprints/lead-ai-score-claude-template.blueprint.json](blueprints/lead-ai-score-claude-template.blueprint.json) | ה-Blueprint של התבנית שייבאתי (בונוס 2) |
| [SPEC.md](SPEC.md) | האפיון של שתי האוטומציות |
| [docs/airtable-setup.md](docs/airtable-setup.md) | הטבלאות והשדות ב-Airtable |
| [docs/tests-invoices.md](docs/tests-invoices.md) | הבדיקות של אוטומציית החשבוניות |
| [docs/tests-leads.md](docs/tests-leads.md) | הבדיקות של אוטומציית הלידים |
| [docs/bonus2-claude-template.md](docs/bonus2-claude-template.md) | בונוס 2: התבנית, מה התאמתי והבדיקה |
| [docs/spec-audit.md](docs/spec-audit.md) | בדיקה של כל סעיף באפיון מול התוצאות |

</div>
