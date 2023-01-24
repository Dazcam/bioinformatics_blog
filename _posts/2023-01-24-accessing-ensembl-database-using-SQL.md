## Accessing ensembl database using SQL

Some basic commands to extract gene and SNP information from Ensembl databases using SQL.

Links: [Home page](https://www.ensembl.org/info/data/mysql.html), [Scehmas](https://www.ensembl.org/info/docs/api/index.html)

```sql
mysql -h ensembldb.ensembl.org -u anonymous -P 5306
use homo_sapiens_variation_108;

SELECT variation.name, variation_feature.consequence_types 
FROM variation, variation_feature 
WHERE variation.variation_id = variation_feature.variation_id and variation.name = "rs...";
```
