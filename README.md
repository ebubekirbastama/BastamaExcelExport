# BastamaExcelExport
<h1>Excel Export Kullanımı</h1>
<p>Eğer açık olarak kullanmak istiyorsanız aşağıdaki gibi kullanabilirsiniz</p>

 ```csharp
using BastamaExcelExport;

class Program
{
    static void Main(string[] args)
    {
        using (EbsExcelExport excelExporter = new EbsExcelExport(true))
        {
            // dataGridView1 verilerini Excel'e aktar
            excelExporter.ExportToExcel(dataGridView1, "C:\\ÇıktıYolu", "DosyaAdı", true);
        }
    }
}
```
<p>Eğer kapalı olarak kullanmak istiyorsanız aşağıdaki gibi kullanabilirsiniz</p>

 ```csharp
using BastamaExcelExport;

class Program
{
    static void Main(string[] args)
    {
        using (EbsExcelExport excelExporter = new EbsExcelExport(false))
        {
            // dataGridView1 verilerini Excel'e aktar
            excelExporter.ExportToExcel(dataGridView1, "C:\\ÇıktıYolu", "DosyaAdı", false);
        }
    }
}
```
