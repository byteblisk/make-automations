<div dir="rtl">

# הכנת Airtable

השלב הזה הוא סעיף 2 בסדר העבודה שב-[SPEC.md](../SPEC.md).

## בסיס חדש: Invoices Inbox

בסיס ייעודי לחשבוניות, כדי שהבסיס של הדשבורד יישאר נקי.

| פרט | ערך |
|---|---|
| Base ID | `appBBtgsEEd383Qyk` |
| טבלה | Invoices |
| Table ID | `tblyxFOYChF4TUjVa` |

השדות נוצרו בדיוק לפי הטבלה בסעיף "הטבלה ב-Airtable" באפיון.

## שדה חדש בטבלת הלידים

בבסיס Leads Dashboard, בטבלה Leads, נוסף שדה נוסחה בשם idNumber. השדה מחזיר את החלק המספרי של id, כדי שתרחיש הלידים ימצא את המספר הגבוה ביותר.

</div>

```text
IF(REGEX_MATCH({id}, '^L-[0-9]+$'), VALUE(SUBSTITUTE({id}, 'L-', '')), 0)
```

<div dir="rtl">

הדשבורד לא קורא את השדה הזה, ולכן הוספתו לא משנה שום דבר במסך.

## שדות לבונוס 2

בטבלה Leads הוספתי שני שדות שאוטומציית בונוס 2 ממלאת: aiScore (מספר, ציון 1 עד 100) ו-aiSummary (טקסט ארוך, סיכום בעברית).

## החיבור מ-Make

ב-Make יצרתי חיבור Airtable מסוג OAuth בשם "ByteBlisk Airtable OAuth connection", עם גישה לשני הבסיסים. יצרתי אותו בהתחברות שלי ל-Airtable, ולכן אין בריפו מפתח או טוקן.

</div>
