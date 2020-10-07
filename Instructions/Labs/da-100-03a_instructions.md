

### 实验室 03A

加载数据至 Power BI Desktop

# 概述

**完成实验室预计需要花费 45 分钟**

在本实验室中，你将开始向上一个实验室中创建的每个查询应用转换。然后，你将应用查询，以将每个查询作为表加载到数据模型。

在本实验室中，你将学习如何：

* 应用不同的转换

* 应用查询以将其加载到数据模型

# 练习 1 ：加载数据

在本练习中，你将把转换应用到上一实验室中创建的每个查询。

*如果不确定自己是否成功完成了上一实验室，可以打开上一个实验室的解决方案文件，该文件位于 **“D:\DA100\Lab02A\Solution”** 文件夹*。

### 任务 1：配置 Salesperson 查询

在此任务中，你将配置 **Salesperson** 查询。

1. 在 **“Power Query Edito”** 窗口的 **“Queries”** 窗格中，选择 **“DimEmployee”** 查询。

    ![图片 1](Linked_image_Files/PowerBI_Lab03A_image1.png)

2. 若要重命名查询，请在 **“查询设置”** 窗格（位于右侧）的 **“名称”** 框中将文本替换为 **“销售人员”**，然后按 **Enter**。

    *查询名称将确定模型表名称。建议定义简洁但友好的名称*。

3. 在 **“查询”** 窗格中，验证查询名称已更新。

    ![图片 87](Linked_image_Files/PowerBI_Lab03A_image2.png)

   *现在，你将过滤查询行，以便只检索作为销售人员的员工*。

4. 要找到特定的列，请在 **“主页”** 功能区选项卡，在 **“管理列”** 组中，单击 **“选择列”** 向下箭头，然后选择 **“转到列”**。

    ![图片 88](Linked_image_Files/PowerBI_Lab03A_image3.png)

    *提示：当查询包含许多列时，此方法很有用。*通常，你只需水平滚动即可找到该列**。

5. 在 **“转到列”** 窗口中，要按列名对列表进行排序，请单击 **AZ** 排序按钮，然后选择 **“名称”**。

    ![图片 94](Linked_image_Files/PowerBI_Lab03A_image4.png)

6. 选择 **“SalesPersonFlag”** 列，然后单击 **“确定”**。

7. 要过滤查询，请在 **“SalesPersonFlag”** 列标题中单击向下箭头，然后取消选中 **“False”**。

    ![图片 95](Linked_image_Files/PowerBI_Lab03A_image5.png)

8. 单击 **“确定”**。

    ![图片 96](Linked_image_Files/PowerBI_Lab03A_image6.png)

9. 在 **“查询设置”** 窗格中的 **“应用的步骤”** 列表中，请注意添加了 **“筛选的行”** 步骤。

    ![图片 98](Linked_image_Files/PowerBI_Lab03A_image7.png)

    *你创建的每个转换都会产生其他步骤逻辑。可以编辑或删除步骤。在转换阶段，还可以选择一个步骤来预览查询结果*。

10. 要删除列，在 **“主页”** 功能区选项卡中的 **“管理列”** 组中，单击 **“选择列”** 图标。

    ![图片 99](Linked_image_Files/PowerBI_Lab03A_image8.png)

11. 在**选择列**窗口中，要取消选中所有列，请取消选中 **（选择所有列）** 项目。

    ![图片 102](Linked_image_Files/PowerBI_Lab03A_image9.png)

12. 要包括列，请选中以下六列：

    * EmployeeKey

    * EmployeeNationalIDAlternateKey

    * FirstName

    * LastName

    * Title

    * EmailAddress

13. 单击 **“确定”**。

    ![图片 104](Linked_image_Files/PowerBI_Lab03A_image10.png)

14. 在 **“应用的步骤”** 列表中，请注意添加了另一个查询步骤。

    ![图片 112](Linked_image_Files/PowerBI_Lab03A_image11.png)

15. 要创建单个名称列，请首先选择 **“FirstName”** 列标题。

16. 按下 **Ctrl** 键的同时，选择 **“LastName”** 列。

    ![图片 116](Linked_image_Files/PowerBI_Lab03A_image12.png)

17. 右键单击任一所选列标题，然后在上下文菜单中选择 **“合并列”**。

    ![图片 117](Linked_image_Files/PowerBI_Lab03A_image13.png)

    *许多常见的转换可以通过右键单击列标题，然后从上下文菜单中选择它们来应用。*但请注意，功能区中提供了所有转换以及更多转换**。

18. 在**合并列**窗口中的 **“分隔符”** 下拉列表中，选择 **“空格”**。

19. 在 **“新列名”** 框中，将文本替换为 **“Salesperson”**。

    ![图片 119](Linked_image_Files/PowerBI_Lab03A_image14.png)

20. 单击 **“确定”**。

    ![图片 5636](Linked_image_Files/PowerBI_Lab03A_image15.png)

21. 若要重命名 **“EmployeeNationalIDAlternateKey”** 列，双击 **“EmployeeNationalIDAlternateKey”** 列标题。

22. 将文本替换为 **“EmployeeID”**，然后按 **Enter**。

    *在被指示重命名列时，应完全按照指示对其进行重命名，这一点很重要*。

23. 使用前面的步骤将 **“EmailAddress”** 列重命名为 **“UPN”**。

    *UPN 是用户主体名称的首字母缩写。在实 **验室 05A** 中配置行级安全性时，将使用此列中的值*。

24. 在状态栏的左下角，验证查询是否有五列和 18 行。

    ![图片 5638](Linked_image_Files/PowerBI_Lab03A_image16.png)

    *如果查询未产生正确的结果，请不要继续进行，否则无法完成后面的实验室，这一点很重要。如果未产生正确的结果，请参考此任务中的步骤解决所有问题*。

### 任务 2：配置 SalespersonRegion 查询

在此任务中，你将配置 **SalespersonRegion** 查询。

1. 在 **“查询”** 窗格中，选择 **“DimEmployeeSalesTerritory”** 查询。

    ![图片 5639](Linked_image_Files/PowerBI_Lab03A_image17.png)

2. 在 **“查询设置”** 窗格中，将查询重命名为 **“SalespersonRegion”**。

3. 要删除最后两列，请先选择 **“DimEmployee”** 列标题。

4. 在按下 **Ctrl** 键的同时，选择 **“DimSalesTerritory”** 列标题。

5. 右键单击任一选择列标题，然后在上下文菜单中选择 **“删除列”**。

    ![图片 5640](Linked_image_Files/PowerBI_Lab03A_image18.png)

6. 在状态栏中，验证查询是否具有两列和 39 行。

    ![图片 5641](Linked_image_Files/PowerBI_Lab03A_image19.png)

### 任务 3：配置 Product 查询

在此任务中，我们将配置 **“Product”** 查询。

*由于实验室中已提供了详细说明，因此，实验室步骤将提供更简洁的说明。*如果需要详细说明，可以参考其他任务**。

1. 选择 **“DimProduct”** 查询。

    ![图片 5643](Linked_image_Files/PowerBI_Lab03A_image20.png)

2. 将该查询重命名为 **“Product”**。

3. 找到 **“FinishedGoodsFlag”** 列，然后筛选该列以检索制成品的产品（即 TRUE）。

4. 删除所有列，以下列除外：

    * ProductKey

    * EnglishProductName

    * StandardCost

    * Color

    * DimProductSubcategory

5. 请注意 **“DimProductSubcategory”** 列代表相关表（它包含 **“值”** 链接）。

6. 在 **“DimProductSubcategory”** 列标题中，在列名称右侧，单击展开按钮。

    ![图片 5644](Linked_image_Files/PowerBI_Lab03A_image21.png)

7. 要取消选中所有列，请取消选中 **“(选择所有列)”** 项目。

8. 选中 **“EnglishProductSubcategoryName”** 和 **“DimProductCategory”** 列。

    ![图片 5646](Linked_image_Files/PowerBI_Lab03A_image22.png)

    *通过选择这两列，将应用转换以联接到 **“DimProductSubcategory”** 表，然后包含这些列。**“DimProductCategory”** 列实际上是另一个相关的表*。

9. 取消选中 **“使用原始列名作为前缀”** 复选框。

    ![图片 5647](Linked_image_Files/PowerBI_Lab03A_image23.png)

    *查询列名称必须始终唯一。选中后，此复选框将为每个列加上扩展列名作为前缀（此处为 **DimProductSubcategory**）。因为已知所选列不会与 **Product** 查询冲突，该选项被取消选择*。

10. 单击 **“确定”**。

    ![图片 5648](Linked_image_Files/PowerBI_Lab03A_image24.png)

11. 请注意，转换产生了两列，并且 **DimProductCategory** 列已被删除。

12. 展开 **DimProductCategory**，然后仅引入 **“EnglishProductCategoryName”** 列。

13. 重命名以下四列：

    * **“EnglishProductName”** 改为 **“Product”**

    * **“StandardCost”** 改为 **“Standard Cost”** （包含一个空格）

    * **“EnglishProductSubcategoryName”** 改为 **“Subcategory”**

    * **EnglishProductCategoryName** 改为 **Category**

14. 在状态栏中，验证查询是否具有 6 列和 397 行。

    ![图片 5651](Linked_image_Files/PowerBI_Lab03A_image25.png)

### 任务 4：配置经销商查询

在此任务中，你将配置**经销商**查询。

1. 选择 **“DimReseller”** 查询。

    ![图片 5653](Linked_image_Files/PowerBI_Lab03A_image26.png)

2. 将查询重命名为 **“Reseller”**。

3. 删除所有列，以下列除外：

    * ResellerKey

    * BusinessType

    * RellerName

    * DimGeography

4. 展开 **“DimGeography”** 列，以便仅包括以下三列：

    * City

    * StateProvinceName

    * EnglishCountryRegionName

    ![Picture 5656](Linked_image_Files/PowerBI_Lab03A_image27.png)

5. 在**业务类型**列标题中，单击向下箭头，然后查看项以及仓库的错误拼写。

    ![图片 2](Linked_image_Files/PowerBI_Lab03A_image28.png)

  
 

6. 右键单击 **“Business Type”** 列标题，然后选择 **“替换值”**。

    ![图片 4](Linked_image_Files/PowerBI_Lab03A_image29.png)

7. 在 **“替换值”** 窗口，配置以下值：

    * 在 **“要查找的值”** 框中，输入 **“Ware House”**

    * 在 **“替换为”** 框，输入 **“Warehouse”**

    ![图片 5](Linked_image_Files/PowerBI_Lab03A_image30.png)

8. 单击 **“确定”**。

    ![图片 6](Linked_image_Files/PowerBI_Lab03A_image31.png)

9. 重命名以下四列：

    * **“BusinessType”** 改为 **“Business Type”** （包含一个空格）

    * **“ResellerName”** 改为 **“Reseller”**

    * **“StateProvinceName”** 改为 **“State-Province”**

    * **“EnglishCountryRegionName”** 改为 **“Country-Region”**

10. 在状态栏中，确认查询具有 6 列和 701 行。

    ![图片 5657](Linked_image_Files/PowerBI_Lab03A_image32.png)

### 任务 5：配置 Region 查询

在此任务中，你将配置 **Region** 查询。

1. 选择 **“DimSalesTerritory”** 查询。

    ![图片 5659](Linked_image_Files/PowerBI_Lab03A_image33.png)

2. 将查询重命名为 **“区域”**。

3. 向 **“销售区域备用密钥”** 列应用筛选器以删除值 0（零）。

    ![图片 5660](Linked_image_Files/PowerBI_Lab03A_image34.png)

4. 删除所有列，以下列除外：

    * SalesTerritoryKey

    * SalesTerritoryRegion

    * SalesTerritoryCountry

    * SalesTerritoryGroup

5. 重命名以下三列：

    * **“SalesTerritoryRegion”** 改为 **“Region”**

    * **“SalesTerritoryCountry”** 改为 **“Country”** 

    * **“SalesTerritoryGroup”** 改为 **“Group”**

6. 在状态栏中，验证查询是否具有四列和 10 行。

    ![图片 5661](Linked_image_Files/PowerBI_Lab03A_image35.png)

### 任务 6：配置 Sales 查询

在此任务中，我们将配置 **“Sales”** 查询。

1. 选择 **FactResellerSales** 查询。

    ![图片 5663](Linked_image_Files/PowerBI_Lab03A_image36.png)

2. 将查询重命名为 **“Sales”**。

3. 删除所有列，以下列除外：

    * SalesOrderNumber

    * OrderDate

    * ProductKey

    * ResellerKey

    * EmployeeKey

    * SalesTerritoryKey

    * OrderQuantity

    * UnitPrice

    * TotalProductCost

    * SalesAmount

    * DimProduct

    *回想一下在实**验室 02A**中，**“FactResellerSales”** 行中有一小部分缺少 **TotalProductCost** 值。包含的 **DimProduct** 列可以检索产品标准成本，以修复缺失值*。

4. 展开 **“DimProduct”** 列，然后包括 **“StandardCost”** 列。

5. 要创建自定义列，请在 **“添加列”** 功能区选项卡上，从 **“常规”** 组内部，单击 **“自定义列”**。

    ![图片 5664](Linked_image_Files/PowerBI_Lab03A_image37.png)

6. 在 **“自定义列”** 窗口的 **“新列名”** 框中，将文本替换为 **“Cost”**。

    ![图片 5665](Linked_image_Files/PowerBI_Lab03A_image38.png)

7. 在 **“自定义列公式”** 框中，输入以下表达式（等号后面的文本）：

8. 为了方便起见，你可以从 **D:\DA100\Lab03A\Assets\Snippets.txt** 文件复制表达式。

    **Power Query**

    ```
    if [TotalProductCost] = null then [OrderQuantity] * [StandardCost] else [TotalProductCost]
    ```

    *此表达式测试 **TotalProductCost** 值是否缺失。如果是，则通过将 **OrderQuantity** 值乘以 **StandardCost** 值生成一个值；否则，它使用现有的 **TotalProductCost** 值*。

9. 单击 **“确定”**。

    ![图片 5666](Linked_image_Files/PowerBI_Lab03A_image39.png)

10. 删除以下两列：

    * TotalProductCost

    * StandardCost

11. 重命名以下三列：

    * **OrderQuantity** 重命名为 **Quantity**

    * **“UnitPrice”** 改为 **“Unit Price”** （包含一个空格）

    * **SalesAmount** 重命名为 **Sales**

12. 要修改列数据类型，请在 **Quantity** 列标题，在列名称的左侧，单击 **1.2** 图标，然后选择 **“整数”**。

    ![图片 5667](Linked_image_Files/PowerBI_Lab03A_image40.png)

    *配置正确的数据类型很重要。当列中包含数值时，如果希望执行数学计算，则选择正确的类型也很重要*。

13. 将以下三列数据类型修改为 **“固定十进制数”**。

    * Unit Price

    * Sales

    * Cost

    ![图片 5668](Linked_image_Files/PowerBI_Lab03A_image41.png)

    *固定十进制数数据类型以全精度存储值，因此需要比十进制数更多的存储空间。*对于财务值或利率（例如汇率），请使用固定十进制数类型，这一点很重要**。

14. 在状态栏中，确认查询具有 10 列和超过 999 行。

    ![图片 5669](Linked_image_Files/PowerBI_Lab03A_image42.png)

    *每个查询最多可加载 1000 行作为预览数据*。

### 任务 7：配置 Targets 查询

在此任务中，我们将配置 **“Targets”** 查询。

1. 选择 **ResellerSalesTargets** 查询。

    ![图片 5672](Linked_image_Files/PowerBI_Lab03A_image43.png)

2. 将查询重命名为 **Targets**。

3. 若要逆透视 12 个月的列 (**“M01”** - **“M12”**)，请先多重选择 **“Year”** 和 **“EmployeeID”** 列标题。

    ![图片 5673](Linked_image_Files/PowerBI_Lab03A_image44.png)

4. 右键单击任一选择列标题，然后在上下文菜单中选择 **“逆透视其他列”**。

    ![图片 5674](Linked_image_Files/PowerBI_Lab03A_image45.png)

5. 请注意，列名称现在显示在 **Attribute** 列中，并且值显示在 **Value** 列中。

6. 将过滤器应用于 **Value** 列以删除连字符 (-) 值。

7. 重命名以下两列：

    * **Attribute** 重命名为 **MonthNumber**（两个词之间没有空格，稍后将删除）

    * **Value** 重命名为 **Target**

    *现在，你将应用转换以生成日期列。日期将来自 **年** 和 **MonthNumber** 列。你将使用 **“示例中的列”** 功能创建列*。

8. 要准备 **MonthNumber** 列值，请右键单击 **MonthNumber** 列标题，然后选择 **“替换值”**。

    ![图片 5676](Linked_image_Files/PowerBI_Lab03A_image46.png)

9. 在 **“替换值”** 窗口的 **“要查找的值”** 框中，输入 **M**。

    ![图片 5677](Linked_image_Files/PowerBI_Lab03A_image47.png)

10. 单击 **“确定”**。

11. 将 **MonthNumber** 列数据类型修改为 **“整数”**。

    ![图片 5678](Linked_image_Files/PowerBI_Lab03A_image48.png)

12. 在 **“添加列”** 功能区选项卡上，从 **“常规”** 组内，单击 **“示例中的列”** 图标。

    ![图片 5675](Linked_image_Files/PowerBI_Lab03A_image49.png)

13. 请注意，第一行对应年份 **“2017”** 和月份 **“7”**。

14. 在 **Column1** 列的第一个网格单元中，开始输入 **2017 年 7 月 1 日**，然后按 **Enter**。

    *该虚拟机使用美国区域设置，因此该日期实际上是 2017 年 7 月 1 日*。

15. 请注意，网格单元格会使用预测值进行更新。

    该功能已准确预测你正在合并两列中的值。

16. 还要注意查询网格上方显示的公式。

    ![图片 5679](Linked_image_Files/PowerBI_Lab03A_image50.png)

17. 要重命名新列，请双击 **Merged** 列标题。

18. 将列重命名为 **TargetMonth**。

    ![图片 5680](Linked_image_Files/PowerBI_Lab03A_image51.png)

19. 单击 **“确定”**。

    ![图片 5681](Linked_image_Files/PowerBI_Lab03A_image52.png)

20. 删除以下列：

    * Year

    * MonthNumber

21. 修改以下列的数据类型：

    * 将 **Target** 修改为固定十进制数

    * 将 **TargetMonth** 修改为日期

22. 要将 **Target** 值乘以 1000，请选择 **“Target”** 列标题，然后在 **“转换”** 功能区选项卡上，从 **“数字列”** 组内，单击 **“标准”**，然后选择 **“乘”**。

    ![图片 5682](Linked_image_Files/PowerBI_Lab03A_image53.png)

23. 在 **“乘”** 窗口中的 **“值”** 框，输入 **1000**。

    ![图片 5683](Linked_image_Files/PowerBI_Lab03A_image54.png)

24. 单击 **“确定”**。

    ![图片 5684](Linked_image_Files/PowerBI_Lab03A_image55.png)

25. 在状态栏中，确认查询具有三列和 809 行。

    ![图片 5685](Linked_image_Files/PowerBI_Lab03A_image56.png)

### 任务 8：配置 ColorFormats 查询

在此任务中，你将配置 **ColorFormats** 查询。

1. 选择 **ColorFormats** 查询。  
	![图片 5687](Linked_image_Files/PowerBI_Lab03A_image57.png)

2. 请注意，第一行包含列名。

3. 在 **“主页”** 功能区选项卡中，单击 **“转换”** 组内的 **“将第一行用作标题”**。  
    ![图片 5688](Linked_image_Files/PowerBI_Lab03A_image58.png)

4. 在状态栏中，确认查询具有三列和 10 行。  
	![图片 5689](Linked_image_Files/PowerBI_Lab03A_image59.png)

### 任务 9：更新 Product 查询

在此任务中，你将通过合并 **ColorFormats** 查询来更新 **Product** 查询。

1. 选择 **“Product”** 查询。  
	![图片 5690](Linked_image_Files/PowerBI_Lab03A_image60.png)

1. 要合并 **ColorFormats** 查询，请在 **“主页”** 功能区选项卡上，从 **“组合”** 组内部，单击 **“合并查询”**。  
	![图片 5654](Linked_image_Files/PowerBI_Lab03A_image61.png)  
	*合并查询允许集成数据，在这种情况下，这些数据来自不同的数据源（SQL Server 和 CSV 文件）*。

1. 在**合并**窗口中的 **“Product”** 查询网格，选择 **“Color”** 列标题。  
	![图片 5655](Linked_image_Files/PowerBI_Lab03A_image62.png)

1. 在 **“Product”** 查询网格下的下拉列表中，选择 **“ColorFormats”** 查询。

1. 在 **ColorFormats** 查询网格，选择 **Color** 列标题。

1. 当 **“私有级别”** 窗口打开时，对于两个数据源中的每一个，在相应的下拉列表中，选择 **“组织”**。  
	![图片 5691](Linked_image_Files/PowerBI_Lab03A_image63.png)  
	*可以为数据源配置私有级别，以确定是否可以在数据源之间共享数据。将每个数据源设置为 **“组织”** 允许它们共享数据（如有必要）。请注意，私有数据源永远不能与其他数据源共享。这并不意味着不能共享私有数据；这意味着 Power Query 引擎无法在数据源之间共享数据*。

1. 单击 **“保存”**。  
	![图片 5692](Linked_image_Files/PowerBI_Lab03A_image64.png)

1. 在 **“合并”** 窗口中，单击 **“确定”**。  
	![图片 5693](Linked_image_Files/PowerBI_Lab03A_image65.png)

1. 展开 **“ColorFormats”** 列以包括以下两列：
    * Background Color Format  
    * Font Color Format

	![图片 5694](Linked_image_Files/PowerBI_Lab03A_image66.png)

1. 在状态栏中，确认查询现在具有 8 列和 397 行。  
	![图片 5695](Linked_image_Files/PowerBI_Lab03A_image67.png)

### 任务 10：更新 ColorFormats 查询

在此任务中，你将更新 **ColorFormats** 以禁用其负载。

1. 选择 **ColorFormats** 查询。  
	![图片 321](Linked_image_Files/PowerBI_Lab03A_image68.png)

2. 在 **“查询设置”** 窗格中，单击 **“所有属性”** 链接。  
	![图片 322](Linked_image_Files/PowerBI_Lab03A_image69.png)

3. 在 **“查询属性”** 窗口中，取消选中 **“启用加载到报表”** 复选框。  
	![图片 323](Linked_image_Files/PowerBI_Lab03A_image70.png)  
	*禁用加载意味着它将不会作为表加载到数据模型。这样做是因为查询已与 Product 查询合并，而 Product 查询已启用以适合数据模型*。

4. 单击 **“确定”**。  
	![图片 324](Linked_image_Files/PowerBI_Lab03A_image71.png)

### 完成

在此任务中，你将完成实验室。

1. 验证你是否有 8 个查询，正确命名如下：

    * Salesperson

    * SalespersonRegion

    * Product

    * Reseller

    * Region

    * Sales

    * Target

    * ColorFormats（不会加载到数据模型中）

2. 要加载数据模型，请在 **“文件”** 后台视图，选择 **“关闭并应用”**。  
	![图片 326](Linked_image_Files/PowerBI_Lab03A_image72.png)  
	*现在，所有启用了加载的查询都已加载到数据模型中*。

3. 在 **“字段”** 窗格（位于右侧）中，请注意已加载到数据模型的七个表。  
	![图片 3](Linked_image_Files/PowerBI_Lab03A_image73.png)

4. 保存 Power BI Desktop 文件。

5. 保持 Power BI Desktop 打开状态。  
	*在下一个实验室中，你将配置数据模型表和关系*。
