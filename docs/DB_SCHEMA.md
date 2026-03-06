# РЎС…РµРјР° Р±Р°Р·С‹ РґР°РЅРЅС‹С…: debt_manager.db

**Р”Р°С‚Р° РѕР±РЅРѕРІР»РµРЅРёСЏ:** 2 РјР°СЂС‚Р° 2026 Рі.

---

## РўР°Р±Р»РёС†Р°: `charges`

**РљРѕР»РёС‡РµСЃС‚РІРѕ Р·Р°РїРёСЃРµР№:** 1 298 591

**РћРїРёСЃР°РЅРёРµ:** РСЃС‚РѕСЂРёСЏ РЅР°С‡РёСЃР»РµРЅРёР№ Рё СЃР°Р»СЊРґРѕ РїРѕ Р»РёС†РµРІС‹Рј СЃС‡РµС‚Р°Рј (Р·Р°РіСЂСѓР¶Р°РµС‚СЃСЏ РёР· DBF С„Р°Р№Р»РѕРІ Р±РёР»Р»РёРЅРіР°).

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | id          | INTEGER   |         0 | nan               |    1 |
|     1 | account_id  | TEXT      |         0 | nan               |    0 |
|     2 | period      | DATE      |         0 | nan               |    0 |
|     3 | charge      | REAL      |         0 | nan               |    0 |
|     4 | saldo       | REAL      |         0 | nan               |    0 |
|     5 | source_file | TEXT      |         0 | nan               |    0 |
|     6 | created_at  | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

**РРЅРґРµРєСЃС‹:**
- `idx_billing_account` вЂ” РїРѕ `account_id`
- `idx_billing_period` вЂ” РїРѕ `period`

---

## РўР°Р±Р»РёС†Р°: `address_linking`

**РљРѕР»РёС‡РµСЃС‚РІРѕ Р·Р°РїРёСЃРµР№:** 36 681

**РћРїРёСЃР°РЅРёРµ:** РЎРїСЂР°РІРѕС‡РЅРёРє Р»РёС†РµРІС‹С… СЃС‡РµС‚РѕРІ СЃ Р¤РРћ Рё Р°РґСЂРµСЃР°РјРё (Р·Р°РіСЂСѓР¶Р°РµС‚СЃСЏ РёР· DBF С„Р°Р№Р»РѕРІ).

**РЎС…РµРјР°:**
|   cid | name         | type      |   notnull | dflt_value        |   pk |
|------:|:-------------|:----------|----------:|:------------------|-----:|
|     0 | id           | INTEGER   |         0 | nan               |    1 |
|     1 | account_id   | TEXT      |         0 | nan               |    1 |
|     2 | fio_raw      | TEXT      |         0 | nan               |    0 |
|     3 | surnames     | TEXT      |         0 | nan               |    0 |
|     4 | address_raw  | TEXT      |         0 | nan               |    0 |
|     5 | address_norm | TEXT      |         0 | nan               |    0 |

**РРЅРґРµРєСЃС‹:**
- `idx_address_linking_norm` вЂ” РїРѕ `address_norm`
- `idx_billing_surnames` вЂ” РїРѕ `surnames`

---

## РўР°Р±Р»РёС†Р°: `raw_fssp`

**РљРѕР»РёС‡РµСЃС‚РІРѕ Р·Р°РїРёСЃРµР№:** 3 732

**РћРїРёСЃР°РЅРёРµ:** РќРѕСЂРјР°Р»РёР·РѕРІР°РЅРЅС‹Рµ РґР°РЅРЅС‹Рµ РёР· С„Р°Р№Р»Р° Р¤РЎРЎРџ.

**РЎС…РµРјР°:**
|   cid | name                   | type      |   notnull | dflt_value        |   pk |
|------:|:-----------------------|:----------|----------:|:------------------|-----:|
|     0 | id                     | INTEGER   |         0 | nan               |    1 |
|     1 | case_number            | TEXT      |         0 | nan               |    0 |
|     2 | case_number_normalized | TEXT      |         0 | nan               |    0 |
|     3 | sum_debt               | REAL      |         0 | nan               |    0 |
|     4 | creditor               | TEXT      |         0 | nan               |    0 |
|     5 | account_id             | TEXT      |         0 | nan               |    0 |
|     6 | debtor_fio             | TEXT      |         0 | nan               |    0 |
|     7 | debtor_address         | TEXT      |         0 | nan               |    0 |
|     8 | debtor_address_norm    | TEXT      |         0 | nan               |    0 |
|     9 | fio_initials           | TEXT      |         0 | nan               |    0 |
|    10 | matching_key           | TEXT      |         0 | nan               |    0 |
|    11 | match_method           | TEXT      |         0 | nan               |    0 |
|    12 | match_confidence       | REAL      |         0 | nan               |    0 |
|    13 | created_at             | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

**РРЅРґРµРєСЃС‹:**
- `idx_fssp_case` вЂ” РїРѕ `case_number_normalized`
- `idx_fssp_matching_key` вЂ” РїРѕ `matching_key`
- `idx_fssp_fio` вЂ” РїРѕ `debtor_fio`

---

## РўР°Р±Р»РёС†Р°: `raw_judgments`

**РљРѕР»РёС‡РµСЃС‚РІРѕ Р·Р°РїРёСЃРµР№:** 5 995

**РћРїРёСЃР°РЅРёРµ:** РќРѕСЂРјР°Р»РёР·РѕРІР°РЅРЅС‹Рµ РґР°РЅРЅС‹Рµ РёР· СЃСѓРґРµР±РЅС‹С… СЂРµРµСЃС‚СЂРѕРІ (Р•РР Р¦, РЈР–РҐ, Р•РРђРЎ).

**РЎС…РµРјР°:**
|   cid | name                   | type      |   notnull | dflt_value        |   pk |
|------:|:-----------------------|:----------|----------:|:------------------|-----:|
|     0 | id                     | INTEGER   |         0 | nan               |    1 |
|     1 | account_id             | TEXT      |         0 | nan               |    0 |
|     2 | case_number            | TEXT      |         0 | nan               |    0 |
|     3 | case_number_normalized | TEXT      |         0 | nan               |    0 |
|     4 | date_start             | DATE      |         0 | nan               |    0 |
|     5 | date_end               | DATE      |         0 | nan               |    0 |
|     6 | sum_main               | REAL      |         0 | nan               |    0 |
|     7 | sum_penalty            | REAL      |         0 | nan               |    0 |
|     8 | sum_duty               | REAL      |         0 | nan               |    0 |
|     9 | source                 | TEXT      |         0 | nan               |    0 |
|    10 | agent                  | TEXT      |         0 | nan               |    0 |
|    11 | status                 | TEXT      |         0 | nan               |    0 |
|    12 | created_at             | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

**РРЅРґРµРєСЃС‹:**
- `idx_judgments_case` вЂ” РїРѕ `case_number_normalized`
- `idx_judgments_account` вЂ” РїРѕ `account_id`

---

## РўР°Р±Р»РёС†Р°: `processed_fssp`

**РћРїРёСЃР°РЅРёРµ:** Р РµР·СѓР»СЊС‚Р°С‚С‹ РѕР±РѕРіР°С‰РµРЅРёСЏ Р¤РЎРЎРџ (Р§Р°СЃС‚СЊ 1).

**РЎС…РµРјР°:**
|   cid | name             | type      |   notnull | dflt_value        |   pk |
|------:|:-----------------|:----------|----------:|:------------------|-----:|
|     0 | id               | INTEGER   |         0 | nan               |    1 |
|     1 | fssp_id          | INTEGER   |         0 | nan               |    0 |
|     2 | case_number      | TEXT      |         0 | nan               |    0 |
|     3 | account_id       | TEXT      |         0 | nan               |    0 |
|     4 | creditor         | TEXT      |         0 | nan               |    0 |
|     5 | period_start     | DATE      |         0 | nan               |    0 |
|     6 | period_end       | DATE      |         0 | nan               |    0 |
|     7 | sum_main         | REAL      |         0 | nan               |    0 |
|     8 | sum_penalty      | REAL      |         0 | nan               |    0 |
|     9 | sum_duty         | REAL      |         0 | nan               |    0 |
|    10 | sum_total        | REAL      |         0 | nan               |    0 |
|    11 | equality_check   | INTEGER   |         0 | nan               |    0 |
|    12 | match_method     | TEXT      |         0 | nan               |    0 |
|    13 | match_confidence | REAL      |         0 | nan               |    0 |
|    14 | created_at       | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

**РњРµС‚РѕРґС‹ СЃРѕРїРѕСЃС‚Р°РІР»РµРЅРёСЏ:**
- `CASE_NUMBER` вЂ” С‚РѕС‡РЅРѕРµ СЃРѕРІРїР°РґРµРЅРёРµ РїРѕ РЅРѕРјРµСЂСѓ РґРµР»Р°
- `FUZZY_CASE_NUMBER` вЂ” РЅРµС‡С‘С‚РєРѕРµ СЃРѕРІРїР°РґРµРЅРёРµ РїРѕ РЅРѕРјРµСЂСѓ РґРµР»Р°
- `COMBINED_CASE_FIO` вЂ” РєРѕРјР±РёРЅРёСЂРѕРІР°РЅРЅРѕРµ СЃРѕРІРїР°РґРµРЅРёРµ (РґРµР»Рѕ + Р¤РРћ)
- `FIO_ADDRESS` вЂ” СЃРѕРІРїР°РґРµРЅРёРµ РїРѕ Р¤РРћ Рё Р°РґСЂРµСЃСѓ

---

## рџ“Љ РЎС…РµРјР° СЃРІСЏР·РµР№ С‚Р°Р±Р»РёС†

```mermaid
erDiagram
    charges ||--o{ address_linking : "РїРѕ account_id"
    raw_fssp ||--o{ processed_fssp : "РѕР±РѕРіР°С‰РµРЅРёРµ"
    raw_judgments ||--o{ processed_fssp : "СЃРѕРїРѕСЃС‚Р°РІР»РµРЅРёРµ"
    raw_judgments ||--o{ processed_segmentation : "СЃРµРіРјРµРЅС‚Р°С†РёСЏ"
    
    charges {
        TEXT account_id PK
        DATE period
        REAL charge
        REAL saldo
    }
    
    address_linking {
        TEXT account_id PK
        TEXT fio_raw
        TEXT address_norm
    }
    
    raw_fssp {
        TEXT case_number_normalized
        REAL sum_debt
        TEXT debtor_fio
    }
    
    raw_judgments {
        TEXT account_id
        TEXT case_number_normalized
        DATE date_end
        REAL sum_main
    }
    
    processed_fssp {
        TEXT case_number
        TEXT account_id
        REAL sum_total
        INTEGER equality_check
    }
    
    processed_segmentation {
        TEXT account_id
        REAL saldo_target
        REAL unjudged_amount
        INTEGER months_depth
    }
```

**РџРѕС‚РѕРє РґР°РЅРЅС‹С…:**

```mermaid
flowchart TD
    A[DBF С„Р°Р№Р»С‹] -->|Р·Р°РіСЂСѓР·РєР°| B[charges + address_linking]
    C[Excel Р¤РЎРЎРџ] -->|Р·Р°РіСЂСѓР·РєР°| D[raw_fssp]
    E[Excel РЎСѓРґРµР±РЅС‹Рµ] -->|Р·Р°РіСЂСѓР·РєР°| F[raw_judgments]
    
    D --> G{РћР±РѕРіР°С‰РµРЅРёРµ Р¤РЎРЎРџ}
    F --> G
    G --> H[processed_fssp]
    
    B --> I{РЎРµРіРјРµРЅС‚Р°С†РёСЏ}
    F --> I
    I --> J[processed_segmentation]
```

---

## РўР°Р±Р»РёС†Р°: `processed_segmentation`

**РљРѕР»РёС‡РµСЃС‚РІРѕ Р·Р°РїРёСЃРµР№:** 26 758

**РћРїРёСЃР°РЅРёРµ:** Р РµР·СѓР»СЊС‚Р°С‚С‹ СЃРµРіРјРµРЅС‚Р°С†РёРё РґРѕР»РіР° (Р§Р°СЃС‚СЊ 2).

**РЎС…РµРјР°:**
|   cid | name             | type      |   notnull | dflt_value        |   pk |
|------:|:-----------------|:----------|----------:|:------------------|-----:|
|     0 | id               | INTEGER   |         0 | nan               |    1 |
|     1 | account_id       | TEXT      |         0 | nan               |    0 |
|     2 | creditor         | TEXT      |         0 | nan               |    0 |
|     3 | cut_off_date     | DATE      |         0 | nan               |    0 |
|     4 | unprocessed_debt | REAL      |         0 | nan               |    0 |
|     5 | months_count     | INTEGER   |         0 | nan               |    0 |
|     6 | total_saldo      | REAL      |         0 | nan               |    0 |
|     7 | created_at       | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

---

## РўР°Р±Р»РёС†Р°: `error_log`

**РћРїРёСЃР°РЅРёРµ:** Р–СѓСЂРЅР°Р» РѕС€РёР±РѕРє РѕР±СЂР°Р±РѕС‚РєРё.

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | id          | INTEGER   |         0 | nan               |    1 |
|     1 | error_type  | TEXT      |         0 | nan               |    0 |
|     2 | account_id  | TEXT      |         0 | nan               |    0 |
|     3 | case_number | TEXT      |         0 | nan               |    0 |
|     4 | source      | TEXT      |         0 | nan               |    0 |
|     5 | message     | TEXT      |         0 | nan               |    0 |
|     6 | created_at  | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

**РўРёРїС‹ РѕС€РёР±РѕРє:**
- `NO_MATCH` вЂ” РЅРµ РЅР°Р№РґРµРЅРѕ СЃРѕРѕС‚РІРµС‚СЃС‚РІРёРµ РїСЂРё РѕР±РѕРіР°С‰РµРЅРёРё Р¤РЎРЎРџ
- `EQUALITY_FAIL` вЂ” СЂР°СЃС…РѕР¶РґРµРЅРёРµ СЃСѓРјРј Р¤РЎРЎРџ Рё СЂР°СЃС‡С‘С‚РЅС‹С…
- `LOAD_ERROR` вЂ” РѕС€РёР±РєР° Р·Р°РіСЂСѓР·РєРё С„Р°Р№Р»Р°
- `SEGMENTATION_ERROR` вЂ” РѕС€РёР±РєР° РїСЂРё СЃРµРіРјРµРЅС‚Р°С†РёРё

---

## РўР°Р±Р»РёС†Р°: `processed_files`

**РћРїРёСЃР°РЅРёРµ:** РўСЂРµРєРµСЂ РѕР±СЂР°Р±РѕС‚Р°РЅРЅС‹С… С„Р°Р№Р»РѕРІ (РґР»СЏ РёРЅРєСЂРµРјРµРЅС‚Р°Р»СЊРЅРѕР№ РѕР±СЂР°Р±РѕС‚РєРё).

**РЎС…РµРјР°:**
|   cid | name          | type      |   notnull | dflt_value        |   pk |
|------:|:--------------|:----------|----------:|:------------------|-----:|
|     0 | id            | INTEGER   |         0 | nan               |    1 |
|     1 | file_name     | TEXT      |         0 | nan               |    0 |
|     2 | file_path     | TEXT      |         0 | nan               |    0 |
|     3 | file_hash     | TEXT      |         0 | nan               |    0 |
|     4 | last_modified | REAL      |         0 | nan               |    0 |
|     5 | records_count | INTEGER   |         0 | nan               |    0 |
|     6 | processed_at  | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

---

## РўР°Р±Р»РёС†Р°: `raw_billing_all`

**РћРїРёСЃР°РЅРёРµ:** РЎС‹СЂС‹Рµ РґР°РЅРЅС‹Рµ РёР· DBF С„Р°Р№Р»РѕРІ (РІСЃРµ 40+ РєРѕР»РѕРЅРѕРє).

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | T0вЂ“T39      | TEXT      |         0 | nan               |    0 |
|    40 | period      | TEXT      |         0 | nan               |    0 |
|    41 | source_file | TEXT      |         0 | nan               |    0 |
|    42 | loaded_at   | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

**РџСЂРёРјРµС‡Р°РЅРёРµ:** РљРѕР»РѕРЅРєРё T0вЂ“T39 СЃРѕРѕС‚РІРµС‚СЃС‚РІСѓСЋС‚ РїРѕР»СЏРј DBF С„Р°Р№Р»Р°.

---

## РўР°Р±Р»РёС†Р°: `raw_fssp_all`

**РћРїРёСЃР°РЅРёРµ:** РЎС‹СЂС‹Рµ РґР°РЅРЅС‹Рµ РёР· Excel С„Р°Р№Р»Р° Р¤РЎРЎРџ (РІСЃРµ РєРѕР»РѕРЅРєРё).

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | id          | INTEGER   |         0 | nan               |    1 |
|     1 | source_file | TEXT      |         0 | nan               |    0 |
|     2 | loaded_at   | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

---

## РўР°Р±Р»РёС†Р°: `raw_uzh_all`

**РћРїРёСЃР°РЅРёРµ:** РЎС‹СЂС‹Рµ РґР°РЅРЅС‹Рµ РёР· Excel С„Р°Р№Р»Р° РЈР–РҐ (РІСЃРµ РєРѕР»РѕРЅРєРё).

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | id          | INTEGER   |         0 | nan               |    1 |
|     1 | source_file | TEXT      |         0 | nan               |    0 |
|     2 | loaded_at   | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

---

## РўР°Р±Р»РёС†Р°: `raw_eirc_ip_all`

**РћРїРёСЃР°РЅРёРµ:** РЎС‹СЂС‹Рµ РґР°РЅРЅС‹Рµ РёР· Excel С„Р°Р№Р»Р° Р•РР Р¦ РРџ (РІСЃРµ РєРѕР»РѕРЅРєРё).

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | id          | INTEGER   |         0 | nan               |    1 |
|     1 | source_file | TEXT      |         0 | nan               |    0 |
|     2 | loaded_at   | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

---

## РўР°Р±Р»РёС†Р°: `raw_eirc_sudy_all`

**РћРїРёСЃР°РЅРёРµ:** РЎС‹СЂС‹Рµ РґР°РЅРЅС‹Рµ РёР· Excel С„Р°Р№Р»Р° Р•РР Р¦ РЎСѓРґС‹ (РІСЃРµ РєРѕР»РѕРЅРєРё).

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | id          | INTEGER   |         0 | nan               |    1 |
|     1 | source_file | TEXT      |         0 | nan               |    0 |
|     2 | loaded_at   | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

---

## РўР°Р±Р»РёС†Р°: `raw_eias_all`

**РћРїРёСЃР°РЅРёРµ:** РЎС‹СЂС‹Рµ РґР°РЅРЅС‹Рµ РёР· Excel С„Р°Р№Р»Р° Р•РРђРЎ (РІСЃРµ РєРѕР»РѕРЅРєРё).

**РЎС…РµРјР°:**
|   cid | name        | type      |   notnull | dflt_value        |   pk |
|------:|:------------|:----------|----------:|:------------------|-----:|
|     0 | id          | INTEGER   |         0 | nan               |    1 |
|     1 | source_file | TEXT      |         0 | nan               |    0 |
|     2 | loaded_at   | TIMESTAMP |         0 | CURRENT_TIMESTAMP |    0 |

---

## РЎРІСЏР·Рё РјРµР¶РґСѓ С‚Р°Р±Р»РёС†Р°РјРё

```
в”Њв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”ђ         в”Њв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”ђ
в”‚   raw_fssp      в”‚         в”‚  raw_judgments   в”‚
в”‚  (Р¤РЎРЎРџ СЂРµРµСЃС‚СЂ)  в”‚в—„в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”‚ (РЎСѓРґРµР±РЅС‹Рµ СЂРµС€РµРЅРёСЏ)в”‚
в””в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”¬в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”  case   в””в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”¬в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”
         в”‚                          в”‚
         в”‚                          в”‚ account_id
         в–ј                          в–ј
в”Њв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”ђ         в”Њв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”ђ
в”‚processed_fssp   в”‚         в”‚    charges       в”‚
в”‚(Р РµР·СѓР»СЊС‚Р°С‚С‹ Р¤РЎРЎРџ)в”‚         в”‚ (РСЃС‚РѕСЂРёСЏ РЅР°С‡РёСЃР».)в”‚
в””в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”         в””в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”¬в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”
                                     в”‚
                                     в”‚ account_id
                                     в–ј
                            в”Њв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”ђ
                            в”‚address_linking   в”‚
                            в”‚ (РЎРїСЂР°РІРѕС‡РЅРёРє Р›РЎ)  в”‚
                            в””в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”¬в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”
                                     в”‚
                                     в”‚ account_id
                                     в–ј
                            в”Њв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”ђ
                            в”‚processed_segment.в”‚
                            в”‚ (РЎРµРіРјРµРЅС‚Р°С†РёСЏ)    в”‚
                            в””в”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”Ђв”
```

---

## РРЅРґРµРєСЃС‹ РґР»СЏ СѓСЃРєРѕСЂРµРЅРёСЏ РїРѕРёСЃРєР°

| РўР°Р±Р»РёС†Р°            | РРЅРґРµРєСЃ                        | РџРѕР»Рµ                |
|:-------------------|:------------------------------|:--------------------|
| raw_judgments      | idx_judgments_case            | case_number_normalized |
| raw_judgments      | idx_judgments_account         | account_id          |
| charges            | idx_billing_account           | account_id          |
| charges            | idx_billing_period            | period              |
| address_linking    | idx_address_linking_norm      | address_norm        |
| address_linking    | idx_billing_surnames          | surnames            |
| raw_fssp           | idx_fssp_case                 | case_number_normalized |
| raw_fssp           | idx_fssp_matching_key         | matching_key        |
| raw_fssp           | idx_fssp_fio                  | debtor_fio          |
""  
"---"  
""  
"## пїЅпїЅпїЅпїЅпїЅпїЅпїЅпїЅ"  
""  
"| [? пїЅ пїЅпїЅаҐ­пїЅ аҐЇпїЅпїЅпїЅпїЅпїЅпїЅ](../README.md) | [?? пїЅпїЅпїЅпїЅпїЅпїЅпїЅ пїЅпїЅпїЅг¬ҐпїЅпїЅпїЅпїЅ](README.md) | [?? пїЅпїЅ](пїЅпїЅ.md) | [?? Changelog](CHANGELOG.md) | [?? пїЅа®ЎпїЅпїЅпїЅпїЅ](пїЅпїЅпїЅпїЅпїЅпїЅпїЅпїЅ.md) |"  
"|:---------------------------------------|:-------------------------------------|:------------------|:----------------------------|:---------------------------|" 
