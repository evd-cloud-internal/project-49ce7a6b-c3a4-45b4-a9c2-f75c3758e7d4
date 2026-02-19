---
name: Home
assetId: af1704f0-f7ca-4105-aac5-4a250f149d3b
type: page
---

# Service Request to Activity Flow

```sql sankey_data
SELECT c1 AS source, c2 || ' (dest)' AS target, c3 AS count
FROM VALUES(
    ('Transportation Services', 'Nutrition Services', 2),
    ('Transportation Services', 'Housing Services', 2),
    ('L2 Navigation', 'No performed activities', 81205),
    ('Housing Services', 'Housing Services', 12882),
    ('L2 Navigation', 'Invalid Code', 4400),
    ('L2 Navigation', 'Housing Services', 1241),
    ('L1 Navigation', 'Housing Services', 324),
    ('L1 Navigation', 'L1 Navigation', 128),
    ('Assessment', 'L2 Navigation', 21),
    ('Assessment', 'Assessment', 61833),
    ('Nutrition Services', 'Invalid Code', 6820),
    ('L2 Navigation', 'Assessment', 17248),
    ('L1 Navigation', 'Nutrition Services', 7),
    ('Transportation Services', 'Invalid Code', 385),
    ('Housing Services', 'L2 Navigation', 262),
    ('Assessment', 'Invalid Code', 3756),
    ('L1 Navigation', 'No performed activities', 4079),
    ('Nutrition Services', 'Assessment', 19),
    ('Housing Services', 'Invalid Code', 2362),
    ('L2 Navigation', 'Nutrition Services', 546),
    ('L2 Navigation', 'L1 Navigation', 91113),
    ('Invalid Code', 'Invalid Code', 3),
    ('L1 Navigation', 'Invalid Code', 122),
    ('Nutrition Services', 'Nutrition Services', 46078),
    ('L1 Navigation', 'Transportation Services', 68),
    ('Assessment', 'L1 Navigation', 15568),
    ('Nutrition Services', 'Housing Services', 1027),
    ('Housing Services', 'No performed activities', 34521),
    ('Transportation Services', 'No performed activities', 9642),
    ('Assessment', 'No performed activities', 36890),
    ('Assessment', 'Housing Services', 416),
    ('Housing Services', 'Assessment', 69),
    ('Invalid Code', 'Assessment', 1),
    ('Invalid Code', 'No performed activities', 72483),
    ('Nutrition Services', 'No performed activities', 81833),
    ('Housing Services', 'L1 Navigation', 19),
    ('Transportation Services', 'Transportation Services', 2043),
    ('Housing Services', 'Nutrition Services', 360),
    ('Nutrition Services', 'L2 Navigation', 2481),
    ('L2 Navigation', 'Transportation Services', 16),
    ('L2 Navigation', 'L2 Navigation', 34871),
    ('Nutrition Services', 'L1 Navigation', 14),
    ('Assessment', 'Transportation Services', 2),
    ('Assessment', 'Nutrition Services', 33),
    ('Invalid Code', 'Housing Services', 1),
    ('Invalid Code', 'L2 Navigation', 1)
) AS t(c1, c2, c3)
```

{% sankey_chart
    data="sankey_data"
    source="source"
    target="target"
    value="sum(count)"
/%}





This Sankey diagram illustrates the flow from service request categories to the activities that were ultimately performed. The widest bands represent the most common pathways, highlighting where the majority of requests end up. Use this visualization to identify bottlenecks, unexpected routing patterns, and opportunities to streamline service delivery.
