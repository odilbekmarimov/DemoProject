| Table ID | File Name | Table Name          | Column Prefix |
| -------- | --------- | ------------------- | ------------- |
| `01`     | `t01.csv` | users               | `01-XX`       |
| `02`     | `t02.csv` | cards               | `02-XX`       |
| `03`     | `t03.csv` | transactions        | `03-XX`       |
| `04`     | `t04.csv` | logs                | `04-XX`       |
| `05`     | `t05.csv` | reports             | `05-XX`       |
| `07`     | `t07.csv` | scheduled\_payments | `07-XX`       |
| `FD`     | Derived   | fraud\_detection    | derived       |
| `VIP`    | Derived   | vip\_users          | derived       |
| `BLK`    | Derived   | blocked\_users      | derived       |



# 🧾 Column Naming Reference

## Users (01-XX)

| Column | Field Name |
|--------|------------|
| `01-01` | name |
| `01-02` | phone_number |
| `01-03` | email |
| `01-04` | created_at |
| `01-05` | last_active_at |
| `01-06` | status |
| `01-07` | is_vip |
| `01-08` | total_balance |

## Cards (02-XX)

| Column | Field Name |
|--------|------------|
| `02-01` | user_id |
| `02-02` | card_number |
| `02-03` | balance |
| `02-04` | is_blocked |
| `02-05` | created_at |
| `02-06` | card_type |
| `02-07` | limit_amount |

## Transactions (03-XX)

| Column | Field Name |
|--------|------------|
| `03-01` | from_card_id |
| `03-02` | to_card_id |
| `03-03` | amount |
| `03-04` | status |
| `03-05` | created_at |
| `03-06` | transaction_type |
| `03-07` | is_flagged |

## Logs (04-XX)

| Column | Field Name |
|--------|------------|
| `04-01` | transaction_id |
| `04-02` | message |
| `04-03` | created_at |

## Reports (05-XX)

| Column | Field Name |
|--------|------------|
| `05-01` | report_type |
| `05-02` | created_at |
| `05-03` | total_transactions |
| `05-04` | flagged_transactions |
| `05-05` | total_amount |

## Scheduled Payments (07-XX)

| Column | Field Name |
|--------|------------|
| `07-01` | user_id |
| `07-02` | card_id |
| `07-03` | amount |
| `07-04` | payment_date |
| `07-05` | status |
| `07-06` | created_at |
