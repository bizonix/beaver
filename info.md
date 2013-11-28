|Filter                        | Operator                      |    Result                                       |
|:-----------------------------|:------------------------------|:------------------------------------------------|
|                              |is blank                       | WHERE "field" =  ''                             |
|                              |is blank or null               | WHERE ("field" = '' OR "field" IS NULL)         |
|                              |is not blank                   | WHERE "field" <> ''                             |
|                              |is not equal to <?>            | WHERE "field" <> 'value'                        |
|`get_if_<PROPERTY>`           |is equal to <?>                | WHERE "field" =  'value'                        |
|`get_if_<PROPERTY>_gt`        |is greater than <?>            | WHERE "field" >  'value'                        |
|`get_if_<PROPERTY>_gte`       |is greater than or equal to <?>| WHERE "field" >= 'value'                        |
|`get_if_<PROPERTY>_lt`        |is less than <?>               | WHERE "field" <  'value'                        |
|`get_if_<PROPERTY>_lte`       |is less than or equal to <?>   | WHERE "field" <= 'value'                        |
|`get_if_<PROPERTY>_startswith`|begin with <?>                 | WHERE "field" LIKE 'value%'                     |
|`get_if_<PROPERTY>_contains`  |contain <?>                    | WHERE "field" LIKE '%value%'                    |
|                              |does not contain <?>           | WHERE NOT ("field" LIKE '%value%')              |
|`get_if_<PROPERTY>_endswith`  |end with <?>                   | WHERE "field" LIKE '%value'                     |
|                              |is not between <?> <?>         | WHERE "field" NOT BETWEEN 'value1' AND 'value2' |
|`get_if_<PROPERTY>_between`   |is between <?> <?>             | WHERE "field" BETWEEN 'value1' AND 'value2'     |
|                              |is not null                    | WHERE "field" IS NOT NULL                       |
|                              |is null                        | WHERE "field" IS NULL                           |
|`get_if_<PROPERTY>_in`        |is in list <?>                 | WHERE "field" IN ('aaa','bbb',...)              |
|`get_if_<PROPERTY>_notin`     |is not in list <?>             | WHERE "field" NOT IN ('aaa','bbb',...)          |


|Filter                        | Operator                      |    Result                                             |
|:-----------------------------|:------------------------------|:------------------------------------------------------|
|`get_if_<PROPERTY>_xbetween`  |is not between <?> <?>         | NOT (("field" >= 'value1') and ("field" <= 'value2')) |
|`get_if_<PROPERTY>_xbetween`  |is not between <?> <?>         | WHERE "field" NOT BETWEEN 'value1' AND 'value2'       |
|`get_if_<PROPERTY>_between`   |is between <?> <?>             | WHERE "field" BETWEEN 'value' AND 'value'             |
|`get_if_<PROPERTY>_between`   |is between <?> <?>             | (("field" >= 'value') and ("field" <= 'value'))       |
|                              |does not contain <?>           | NOT LIKE '%value%'                                    |
