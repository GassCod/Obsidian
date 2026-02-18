---
tags:
  - Dictionary
  - Templates
---
# <% tp.file.title %>

**Перевод:** <%*
const title = tp.file.title;
const url = `https://translate.googleapis.com/translate_a/single?client=gtx&sl=en&tl=ru&dt=t&dt=md&q=${encodeURI(title)}`;
const response = await fetch(url);
const data = await response.json();
const translation = data[0][0][0];
tR += translation;
%>

### Значение
<%*
let definitions = "";
if (data[12]) {
    data[12].forEach(cat => {
        definitions += `**${cat[0]}**:\n`;
        cat[1].forEach(def => { definitions += `* ${def[0]}\n`; });
    });
} else { definitions = "_Определение не найдено_"; }
tR += definitions;
%>

---
**Связи:** [[Main Dictionary Page|Назад в словарь]]