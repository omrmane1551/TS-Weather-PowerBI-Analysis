- Marked Date Table to enable accurate time intelligence

---

## 📐 Key DAX Measures
```DAX
Avg Temperature = AVERAGE ( Weather_Fact[Avg Temperature] )

Total Rainfall = SUM ( Weather_Fact[Rainfall] )

Rainfall LY =
CALCULATE (
  [Total Rainfall],
  SAMEPERIODLASTYEAR ( Date_Table[Date] )
)

Rainfall YoY % =
DIVIDE (
  [Total Rainfall] - [Rainfall LY],
  [Rainfall LY]
)
