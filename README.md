# logical-query-nosql
1. $and: Buku dengan stok > 2 dan tahun ≥ 2021
{
  "$and": [
    { "stok": { "$gt": 2 } },
    { "tahun": { "$gte": 2021 } }
  ]
}
2. $or: Buku kategori "Matematika" atau stok < 3
{
  "$or": [
    { "kategori": "Matematika" },
    { "stok": { "$lt": 3 } }
  ]
}
3. $not: Buku dengan stok tidak lebih dari 2
{
  "stok": { "$not": { "$gt": 2 } }
}
4. $nor: Buku yang bukan kategori Matematika dan bukan stok < 3
{
  "$nor": [
    { "kategori": "Matematika" },
    { "stok": { "$lt": 3 } }
  ]
