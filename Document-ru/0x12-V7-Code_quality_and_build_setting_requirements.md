# V7: Требования к качеству кода и настройкам сборки

## Цель контроля

Следование требованиям данного раздела обеспечивает использование базовых практик безопасного написания кода при разработке приложения, а также стандартных средств безопасности, встроенных в компилятор.

## Требования безопасности

| # | MSTG-ID | Описание || L2 |
| --- | --- | --- | --- | --- |
| **7.1** | MSTG‑CODE‑1 | Приложение подписано валидным сертификатом. | ✓ | ✓ |
| **7.2** | MSTG‑CODE‑2 | Приложение было собрано в release режиме с настройками, подходящими для релизной сборки (например, без атрибута debuggable). | ✓ | ✓ |
| **7.3** | MSTG‑CODE‑3 | Отладочные символы удалены из нативных бинарных файлов. | ✓ | ✓ |
| **7.4** | MSTG‑CODE‑4 | Отладочный код был удален, и приложение не логирует подробные ошибки и отладочные сообщения. | ✓ | ✓ |
| **7.5** | MSTG‑CODE‑5 | Все сторонние компоненты, используемые мобильным приложением (библиотеки и фреймворки), идентифицированы и проверены на наличие известных уязвимостей. | ✓ | ✓ |
| **7.6** | MSTG‑CODE‑6 | Приложение обрабатывает возможные исключения.| ✓ | ✓ |
| **7.7** | MSTG‑CODE‑7 | В логике обработки связанных с безопасностью ошибок по умолчанию запрещается доступ. | ✓ | ✓ |
| **7.8** | MSTG‑CODE‑8 | В неконтролируемом коде память выделяется, освобождается и используется безопасно.  | ✓ | ✓ |
| **7.9** | MSTG‑CODE‑9 | Активированы все стандартные функции безопасности, предусмотренные инструментами разработчика (такие как минификация байт-кода, защита стека, поддержка PIE и ARC). | ✓ | ✓ |

<div style="page-break-after: always;">
</div>

## Ссылки

OWASP MSTG содержит подробные инструкции по проверке требований, перечисленных в этом разделе.

- Android - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05i-Testing-Code-Quality-and-Build-Settings.md>
- iOS - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05i-Testing-Code-Quality-and-Build-Settings.md>

Для получения дополнительной информации смотрите также:

- OWASP Mobile Top 10: M7 - Poor Code Quality: <https://www.owasp.org/index.php/Mobile_Top_10_2016-M7-Poor_Code_Quality>
- CWE: <https://cwe.mitre.org/data/definitions/119.html>
- CWE: <https://cwe.mitre.org/data/definitions/89.html>
- CWE: <https://cwe.mitre.org/data/definitions/388.html>
- CWE: <https://cwe.mitre.org/data/definitions/489.html>
