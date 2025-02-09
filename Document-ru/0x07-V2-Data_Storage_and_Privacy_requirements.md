# V2: Требования к конфиденциальности и хранению данных

## Цель проверки

Защита чувствительных данных, таких, как данные пользователя для авторизации (логин + пароль) и персональные данные, является ключевым аспектом в безопасности мобильных приложений. Во-первых, чувствительные данные могут  быть непреднамеренно раскрыты другим приложениям, работающим на том же устройстве, если механизмы операционной системы, такие как межпроцессное взаимодействие (IPC), используются ненадлежащим образом. Данные также могут непреднамеренно попасть в облачное хранилище, резервную копию или кеш клавиатуры. Кроме того, мобильные устройства могут быть потеряны или украдены легче чем другие типы устройств, поэтому злоумышленник, получивший физический доступ к устройству, является наиболее вероятным сценарием. В этом случае могут быть реализованы дополнительные меры защиты для затруднения извлечения чувствительных данных с устройства.

Следует обратить внимание, что MASVS ориентирован на приложения, и потому не охватывает политики безопасности на уровне устройства (MDM - Mobile Device Managment). Мы поощряем использование таких политик в контексте предприятия для повышения безопасности данных.

### Определение чувствительных данных

К чувствительным данным в контексте MASVS относятся как данные пользователя для авторизации, так и любые другие данные, которые считаются чувствительными в конкретном контексте, например:

- Персональные данные, которые могут быть использованы для кражи личности: номера социального страхования, кредитных карт, банковских счетов, информация о здоровье.
- Конфиденциальная информация, которая может привести к репутационному ущербу и/или финансовым потерям, если она скомпрометирована: информация о договорах, информация, охватываемая соглашениями о неразглашении, управленческая информация;
- Любые данные, которые должны быть защищены по закону или внутренним требованиям компании.

<div style="page-break-after: always;">
</div>

## Требования безопасности

Подавляющее большинство проблем с раскрытием информации можно предотвратить, следуя простым правилам. Большинство требований, перечисленных в этой главе, являются обязательными для всех уровней проверки.

| # | MSTG-ID | Описание | L1 | L2 |
| --- | --- | --- | --- | --- |
| **2.1** | MSTG‑STORAGE‑1 | Хранилище учетных данных системы используется надлежащим образом для хранения чувствительных данных, таких как персональные данные, данные пользователя для авторизации и криптографические ключи. | ✓ | ✓ |
| **2.2** | MSTG‑STORAGE‑2 | Чувствительные данные хранятся только во внутреннем хранилище приложения, либо в системном хранилище авторизационных данных. | ✓ | ✓ |
| **2.3** | MSTG‑STORAGE‑3 | Чувствительные данные не попадают в логи приложения. | ✓ | ✓ |
| **2.4** | MSTG‑STORAGE‑4 | Никакие чувствительные данные не передаются третьей стороне, если это не является необходимой частью архитектуры. | ✓ | ✓ |
| **2.5** | MSTG‑STORAGE‑5 | Кэш клавиатуры выключен для полей ввода чувствительных данных. | ✓ | ✓ |
| **2.6** | MSTG‑STORAGE‑6 | Буфер обмена выключен для текстовых полей, которые могут содержать чувствительные данные. | ✓ | ✓ |
| **2.7** | MSTG‑STORAGE‑7 | Чувствительные данные недоступны для механизмов межпроцессного взаимодействия (IPC). | ✓ | ✓ |
| **2.8** | MSTG‑STORAGE‑8 | Никакие чувствительные данные, такие как пароли или пин-коды, не видны через пользовательский интерфейс. | ✓ | ✓ |
| **2.9** | MSTG‑STORAGE‑9 | Никакие чувствительные данные не попадают в бэкапы, создаваемые операционной системой. |   | ✓ |
| **2.10** | MSTG‑STORAGE‑10 | Приложение скрывает чувствительные данные с экрана, когда находится в фоновом режиме. |  | ✓ |
| **2.11** | MSTG‑STORAGE‑11 | Приложение не хранит чувствительные данные в памяти дольше, чем необходимо, и полностью удаляет их из памяти после работы с ними. |  | ✓ |
| **2.12** | MSTG‑STORAGE‑12 | Приложение требует от пользователя минимальную настройку доступа к устройству, такую, как установку пин-кода на устройство. |  | ✓ |
| **2.13** | MSTG‑STORAGE‑13 | Приложение информирует пользователя о персональных данных, которые оно обрабатывает, а также о лучших практиках безопасности, которым должен следовать пользователь при использовании приложения. |  | ✓ |

<div style="page-break-after: always;">
</div>

## Ссылки

OWASP MSTG содержит подробные инструкции по верификации требований, перечисленных в этом разделе.

- Для Android - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05d-Testing-Data-Storage.md>
- Для iOS - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06d-Testing-Data-Storage.md>

Для получения дополнительной информации смотрите также:

- OWASP Mobile Top 10: M2 - Insecure Data Storage: <https://www.owasp.org/index.php/Mobile_Top_10_2016-M2-Insecure_Data_Storage>
- CWE: <https://cwe.mitre.org/data/definitions/922.html>
