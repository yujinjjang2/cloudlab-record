# SQL 기본 DML 구조

## 조회

```sql
Select
    a.COLUMN_NAME  -- 조회 항목
From
    TABLE_NAME a
Where 1 = 1
And a.COLUMN_NAME = #{VALUE};
```

## 삽입

```sql
Insert Into TABLE_NAME
(
    COLUMN_NAME
)
Values
(
    #{VALUE}
);
```

## 수정과 삭제

```sql
Update TABLE_NAME
Set
    COLUMN_NAME = #{VALUE}
Where 1 = 1
And PRIMARY_KEY = #{PRIMARY_KEY};

Delete
From TABLE_NAME
Where 1 = 1
And PRIMARY_KEY = #{PRIMARY_KEY};
```

수정·삭제 전에는 동일한 조건의 `Select`로 대상 행을 먼저 확인하고, 트랜잭션 범위와 영향 건수를 점검한다.

