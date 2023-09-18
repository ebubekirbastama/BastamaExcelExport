# BastamaExcelExport

## Excel Export Kullanımı

Bu kütüphane, Excel verileri aktarmak için kullanışlı bir yol sunar. Aşağıdaki örneklerde nasıl kullanılacağını görebilirsiniz.

### Açık Kullanım

Aşağıdaki örnek, Excel verilerini açık bir şekilde aktarmak için kullanılır:

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
### Kapalı Kullanım
Aşağıdaki örnek, Excel verilerini kapalı bir şekilde aktarmak için kullanılır:

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
# Excel Export Kullanım Videosu
[![Video Adı](https://img.youtube.com/vi/KmUc8y01DrM/0.jpg)](https://www.youtube.com/watch?v=KmUc8y01DrM)





# Excel İmport Kullanımı

Bu kütüphane, bir Excel dosyasından veri okuyarak bir DataTable döndürmenizi sağlar. Daha sonra bu veriyi DataGridView, ListBox, ListView gibi bileşenlere aktarabilirsiniz.

Aşağıdaki örnek, Excel verilerini bir DataGridView kontrolüne aktaran temel bir kod parçası sunar:

## Kullanım Örneği

Aşağıda, bu yöntemi kullanarak Excel verilerini bir DataGridView kontrolüne aktaran örnek bir kod parçası bulunmaktadır:

```csharp
using (ExcelReader excelReader = new ExcelReader("EBSHarita_Cikti_Verisi.xlsx"))
{
    DataTable data = excelReader.ReadData();
    dataGridView1.DataSource = data;
}
```
# Excel İmport Kullanım Videosu
[![Video Adı](https://img.youtube.com/vi/KmUc8y01DrM/0.jpg)](https://www.youtube.com/watch?v=igKivQL66gM)
