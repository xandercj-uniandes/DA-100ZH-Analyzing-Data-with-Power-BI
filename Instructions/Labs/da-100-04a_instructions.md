

### 实验室 04A

Power BI Desktop 中的数据建模

# 概述

**完成实验室预计需要花费 45 分钟**

在本实验室中，你将开始开发数据模型。这涉及在表之间创建关系，然后配置表和列属性，以提高数据模型的友好性和可用性。你还将创建层次结构并创建快速度量。

在本实验室中，你将学习如何：

* 创建模型关系

* 配置表和列属性

* 创建层次结构

* 制定快速度量

# 练习 1 ：创建模型关系

在此练习中，你将创建模型关系。

如果不确定自己是否成功完成了上一个实验室，可以打开上一个实验室的解决方案文件，该文件位于 **“D:\DA100\Lab03A\Solution”** 文件夹。

### 任务 1：创建模型关系

在此任务中，你将创建模型关系。

1. 在 Power BI Desktop中，单击左侧的**模型**视图图标。

	![图片 1](Linked_image_Files/PowerBI_Lab04A_image1.png)

2. 如果不能看到所有七个表，可以向右水平滚动，然后将这些表拖放到一起，这样就可以同时看到它们。

	*在模型视图中，可以查看每个表和关系（表之间的连接器）。*目前，没有任何关系存在，因为你在实**验室 02A** 中禁用了数据加载关系选项*。

3. 若要返回报表视图，请在左侧单击**报表**视图图标。

	![图片 327](Linked_image_Files/PowerBI_Lab04A_image2.png)

4. 若要查看所有表字段，请右键单击**字段**窗格中空白区域，然后选择 **“展开全部”**。

	![图片 328](Linked_image_Files/PowerBI_Lab04A_image3.png)

5. 要创建“表”视觉对象，请在 **“字段”** 窗格中检查 **“Product”** 表内的 **“Category”** 字段。

	![图片 329](Linked_image_Files/PowerBI_Lab04A_image4.png)

	*从现在开始，实验室将使用速记表示法来引用字段。就像这样：**产品 | Category***。

6. 若要在表中添加列，请检查 **“字段”** 窗格中的 **“Sales | Sales”** 字段也是如此。

7. 请注意，表视觉对象列出了四个产品类别，每个类别的销售额值相同，总计也相同。

	![图片 330](Linked_image_Files/PowerBI_Lab04A_image5.png)

	*问题在于该表基于不同表中的字段。期望每个产品类别都显示该类别的销售额。但是，由于这些表之间没有模型关系，**“Sales”** 表未经过筛选。*现在你将添加一个关系，以在表之间传播筛选器*。

8. 在 **“建模”** 功能区选项卡上，单击 **“关系”** 功能组内的 **“管理关系”**。

	![图片 331](Linked_image_Files/PowerBI_Lab04A_image6.png)

9. 在 **“管理关系”** 窗口中，可以看到尚未定义任何关系。

10. 若要创建关系，请单击 **“新建”**。

	![图片 332](Linked_image_Files/PowerBI_Lab04A_image7.png)

11. 在 **“创建关系”** 窗口的第一个下拉列表中，选择 **“Product”** 表。

	![图片 333](Linked_image_Files/PowerBI_Lab04A_image8.png)

12. 在第二个下拉列表中（ **“产品”** 网格型下方），选择 **“Sales”** 表。

	![图片 334](Linked_image_Files/PowerBI_Lab04A_image9.png)

13. 可以看到每个表中的 **“产品键”** 列均已选中。

	*由于这些列共享相同的名称，因此自动选中*。

14. 在 **“基数”** 下拉列表中，可以看到已选择 **“一对多”**。

	*该基数是自动检测到的，因为 Power BI 知道 **Product** 表中的  **ProductKey** 列包含唯一值。*一对多关系是最常见的基数，本实验室中创建的所有关系都将是这种类型。你将在实**验室 05A** 中使用多对多基数*。

15. 在 **“交叉筛选方向”** 下拉列表中，可以看到 **“单向”** 已选中。

	*单一筛选方向表示筛选器从“一侧”传播到“多侧”。在本例中，这意味着应用于 **“Product”** 表的筛选器将传播到 **“Sales”** 表，但传播方向不能反过来。你将在实**验室 05A**中使用双向关系*。

16. 可以看到 **“将此关系标记为可用”** 处于选中状态。

	*主动关系将传播筛选器。可以将关系标记为非活动状态，这样筛选器就不会传播。当表之间存在多个关系路径时，可能存在不活动的关系。在这种情况下，模型计算可以使用特殊功能来激活它们。你将在实**验室 05A**中使用非活动关系*。

17. 单击 **“确定”**。

	![图片 335](Linked_image_Files/PowerBI_Lab04A_image10.png)

18. 在**管理关系**窗口中，请注意新关系已列出，然后单击 **“关闭”**。

	![图片 336](Linked_image_Files/PowerBI_Lab04A_image11.png)

19. 在报表中，可以看到表视觉对象已更新为每个产品类别显示不同的值。

	![图片 337](Linked_image_Files/PowerBI_Lab04A_image12.png)

20. 应用于 **“Product”** 表的筛选器现在传播到了 **“Sales”** 表。

21. 切换到模型视图，然后可以看到两个表之间现在有一个连接器。

	![图片 338](Linked_image_Files/PowerBI_Lab04A_image13.png)

22. 在下图中，注意你可以解释由 **1** 和 ***** 指标表示的基数。

	*筛选器的方向由箭头表示。并且，实线表示活动关系，虚线表示非活动关系*。

23. 将光标悬停在关系上以显示相关列。

	*创建关系还有更简单的方法。在模型示意图中，可以对列进行拖放以创建新关系*。

24. 若要创建新关系，请将 **“Reseller”** 表中的 **“ResellerKey”** 列拖放到 **“Sales”** 表中的 **“ResellerKey”** 列上。

	![图片 339](Linked_image_Files/PowerBI_Lab04A_image14.png)

	*提示：有时候，有的列无法正常拖动。*如果出现这种情况，请选择其他列，再选择打算拖动的列，然后再次尝试拖动*。

25. 创建以下两个模型关系：

	* **“Region | SalesTerritoryKey”** 到 **“Sales | SalesTerritoryKey”**

	* **“Salesperson | EmployeeKey”** 到 **“Sales | EmployeeKey”**

	*在此实验室中，**“SalespersonRegion”** 和 **“Targets”** 表将保持断开。*销售人员与区域之间存在多对多关系，你将在下一个实验室中使用这种高级方案*。

26. 下图中显示了各表的放置，其中将 **“Sales”** 表放置于中心位置，并排列与之关联的表。

	![图片 340](Linked_image_Files/PowerBI_Lab04A_image15.png)

27. 保存 Power BI Desktop 文件。

# 练习 2：配置表

在本练习中，你将通过创建层次结构和对列进行隐藏、格式化和分类来配置每个表。

### 任务 1：配置“Product”表

在此任务中，你将配置 **“Product”** 表。

1. 在“模型”视图中的 **“字段”** 窗格中，展开 **“Product”** 表（如有必要）。

2. 要创建层次结构，请在 **“字段”** 窗格中右键单击 **“Category”** 列，然后选择 **“创建层次结构”**。

	![图片 341](Linked_image_Files/PowerBI_Lab04A_image16.png)

3. 在 **“属性”** 窗格（ **“字段”** 窗格左侧）中，将 **“名称”** 框中的文本替换为 **“Products”**。

	![图片 344](Linked_image_Files/PowerBI_Lab04A_image17.png)

4. 若要向层次结构添加第二个级别，请在 **“层次结构”** 下拉列表中选择 **“子类别”**。

5. 要向层次结构添加第三个级别，请在 **“层次结构”** 下拉列表中选择 **“Product”**。

6. 要完成层次结构设计，请单击 **“应用级别更改”**。

	![图片 343](Linked_image_Files/PowerBI_Lab04A_image18.png)

	*提示：务必单击 **“应用级别更改”**，忽略此步骤是一种常见错误*。

7. 在**字段**窗格中，请注意 **“Products”** 层次结构。

	![图片 347](Linked_image_Files/PowerBI_Lab04A_image19.png)

8. 若要显示层次结构级别，请展开 **Products** 层次结构。

	![图片 346](Linked_image_Files/PowerBI_Lab04A_image20.png)

9. 若要将列组织到一个显示文件夹中，请先选择**字段**窗格中的 **“背景颜色格式”** 列。

10. 按住 **Ctrl** 键，然后选择 **“字体颜色格式”**。

11. 在**属性**窗格中的 **“显示文件夹”** 框内，输入 **“格式”**。

	![图片 348](Linked_image_Files/PowerBI_Lab04A_image21.png)

12. 在 **“字段”** 窗格中，注意这两列现在位于一个文件夹中。

	![图片 349](Linked_image_Files/PowerBI_Lab04A_image22.png)

	*使用显示文件夹是整理表的一种好方法，尤其是对于那些包含很多字段的表来说*。

### 任务 2：配置 Region 表

在此任务中，我们将配置 **“Region”** 表。

1. 在 **“Region”** 表中，创建一个名为 **“区域”** 的层次结构，分为以下三个级别：

	* 组

	* Country

	* Region

	![图片 350](Linked_image_Files/PowerBI_Lab04A_image23.png)

2. 选择 **“Country”** 列（不是 **“Country”** 级别）。

3. 在 **“属性”** 窗格中，展开 **“高级”** 部分，然后选择 **“数据类别”** 下拉列表中的 **“国家/区域”**。

	![图片 352](Linked_image_Files/PowerBI_Lab04A_image24.png)

	*数据分类可以为报表设计者提供提示。本例将列分类为国家或区域，可在呈现地图可视化效果时提供更准确的信息*。

### 任务 3：配置“Reseller”表

在此任务中，我们将配置 **“Reseller”** 表。

1. 在 **“Reseller”** 表中，创建一个名为 **“经销商”** 的层次结构，分为以下两个级别：

	* 商业类型

	* 经销商

	![图片 351](Linked_image_Files/PowerBI_Lab04A_image25.png)

2. 创建第二个层次结构，命名为 **“Geography”**，分为以下四个级别：

	* Country-Region

	* State-Province

	* City

	* Reseller

	![图片 353](Linked_image_Files/PowerBI_Lab04A_image26.png)

3. 将以下三列分类：

	* 将 **“Country-Region”** 分类为 **“Country/Region”**

	* 将 **“State-Province”** 分类为 **“State or Province”**

	* 将 **“City”** 分类为 **“City”**

### 任务 4：配置“Sales”表

在此任务中，我们将配置 **“Sales”** 表。

1. 在 **“Sales”** 表中，选择 **“Cost”** 列。

2. 在 **“属性”** 窗格中的 **“描述”** 框内输入：**依据标准成本**

	![图片 358](Linked_image_Files/PowerBI_Lab04A_image27.png)

	*说明可应用于表、列、层次结构或度量。在 **“字段”** 窗格中，当报表作者将光标悬停在字段上时，说明文本就会显示在工具提示中*。

3. 选择 **“Quantity”** 列。

4. 在 **“属性”** 窗格中的 **“格式”** 部分内，将 **“千位分隔符”** 属性滑动至 **“开”**。

	![图片 357](Linked_image_Files/PowerBI_Lab04A_image28.png)

5. 选择 **“单价”** 列。

6. 在 **“属性”** 窗格的 **“格式设置”** 部分，将 **“小数位数”** 属性滑动至 **“2”**。

7. 在 **“高级”** 组（可能需要向下滚动才能找到）的 **“汇总方式”** 下拉列表中选择 **“平均值”**。

	![图片 354](Linked_image_Files/PowerBI_Lab04A_image29.png)

	*默认情况下，数字列通过将值相加进行汇总。此默认行为不适用于 **“Unit Price”** 之类的代表比率的列。将默认汇总设置为平均值，将产生准确有用的结果*。

### 任务 5：批量更新属性

在此任务中，将在单个批量更新中更新多个列。将使用此方法来隐藏列，并设置列值的格式。

1. 在按下 **Ctrl** 键时，选择以下 13 个列（跨多个表）：

	* 产品 | ProductKey

	* Region | SalesTerritoryKey

	* Reseller | ResellerKey

	* Sales | EmployeeKey

	* Sales | ResellerKey

	* Sales | SalesOrderNumber

	* Sales | SalesTerritoryKey

	* Salesperson | EmployeeID

	* Salesperson | EmployeeKey

	* Salesperson | UPN

	* SalespersonRegion | EmployeeKey

	* SalespersonRegion | SalesTerritoryKey

	* Targets | EmployeeID

2. 在 **“属性”** 窗格中将 **“隐藏”** 属性滑动至 **“开”**。

	![图片 355](Linked_image_Files/PowerBI_Lab04A_image30.png)

	*这些列是隐藏的，因为它们要么被关系使用，要么将在行级安全性配置或计算逻辑中使用*。

	*将在下一个实验室中使用 **“UPN”** 列来定义行级安全性。将在实**验室 06A** 中使用 **“SalesOrderNumber”** 进行计算*。

3. 多选以下列：

	* Product | Standard Cost

	* Sales | Cost

	* Sales | Sales 

4. 在 **“属性”** 窗格中，从 **“格式设置”** 部分内将 **“小数位数”** 属性设置为 **“0”** （零）。

	![图片 356](Linked_image_Files/PowerBI_Lab04A_image31.png)

# 练习 3：查看模型接口

在本练习中，将切换到“报表”视图，查看模型接口。

### 任务 1：查看模型接口

在此任务中，将切换到“报表”视图，查看模型接口。

1. 切换到“报表”视图。

2. 请注意在 **“字段”** 窗格中：

	* 列、层次结构及其级别均为字段，可用于配置报表视觉对象

	* 只有与报表创作相关的字段才可见

	*  **“SalespersonRegion”** 表不可见 - 因为其所有字段都被隐藏

	*  **“Region”** 和 **“Reseller”** 表中的空间字段配有空间图标

	* 默认情况下，配有 sigma 符号 (Ʃ) 的字段将进行汇总

	* 将光标悬停在 **“Sales”** 上会出现工具提示 | **“Cost”** 字段

3. 展开 **“Sales”** | **OrderDate”** 字段，然后注意其展示了一个日期层次结构。

	![图片 359](Linked_image_Files/PowerBI_Lab04A_image32.png)

	* **“Targets | TargetMonth”** 呈现相同的层次结构。这些层次结构不是由你创建。它们是自动创建的。但是，有一个问题。Adventure Works 财政年度始于每年的 7 月 1 日。*但是，日期层次结构的年份始于每年的 1 月 1 日*。

	*现将关闭此自动行为。将在 **“实验室 06A”** 中使用 DAX 创建日期表，并对其进行配置以定义 Adventure Works 的日历*。

4. 单击 **“文件”** 功能区选项卡打开 backstage 视图即可关闭自动/日期时间。

5. 选择左侧的 **“选项和设置”**，然后选择 **“选项”**。

	![图片 360](Linked_image_Files/PowerBI_Lab04A_image33.png)

6. 在**选项**窗口左侧的 **“当前文件”** 组中选择 **“数据加载”**。

	![图片 361](Linked_image_Files/PowerBI_Lab04A_image34.png)

7. 在 **“时间智能”** 部分，取消选中 **“自动日期/时间”**。

	![图片 362](Linked_image_Files/PowerBI_Lab04A_image35.png)

8. 单击 **“确定”**。

	![图片 9](Linked_image_Files/PowerBI_Lab04A_image36.png)

9. 请注意 **“字段”** 窗格中的日期层次结构不再可用。

	![图片 363](Linked_image_Files/PowerBI_Lab04A_image37.png)

# 练习 4：创建快速度量

在本练习中，将创建两个快速度量。

### 任务 1：制定快速度量

在此任务中，将创建两个快速度量来计算利润和利润率。

1. 右键单击 **“字段”** 窗格中的 **“Sales”** 表，然后选择 **“新建快速度量”**。

	![图片 366](Linked_image_Files/PowerBI_Lab04A_image38.png)

2. 在 **“快速度量值”** 窗口的 **“计算”** 下拉列表中，从 **“数学运算”** 组内选择 **“减法”**。

	![图片 367](Linked_image_Files/PowerBI_Lab04A_image39.png)

3. 在 **“字段”** 窗格中展开 **“销售额”** 表。

4. 将 **“销售额”** 字段拖到 **“基值”** 框内。

5. 将 **“Cost”** 字段拖动到 **“要减去的值”** 框内。

	![图片 368](Linked_image_Files/PowerBI_Lab04A_image40.png)

6. 单击 **“确定”**。

	![图片 369](Linked_image_Files/PowerBI_Lab04A_image41.png)

	*快度量值为你创建计算。对于简单而通用的计算，可以轻松快速地创建。将使用实**验室 06A** 中的公式语言（而非此工具）创建度量值*。

7. 注意 **“字段”** 窗格 **“Sales”** 表中新的度量值。

	![图片 370](Linked_image_Files/PowerBI_Lab04A_image42.png)

	*各度量均带有计算器图标*。

8. 若要重命名度量，请右键单击度量，然后选择 **“重命名”**。

	![图片 371](Linked_image_Files/PowerBI_Lab04A_image43.png)

	*提示：若要重命名字段，你也可以双击字段，或选择字段并按 **F2***。

9. 将度量重命名为 **“利润”**，然后按 **Enter**。

10. 在 **“Sales”** 表中，根据以下要求添加第二个快速度量：

	* 使用 **“除法”** 数学运算

	* 将 **“分子”** 设为 **“Sales | Sales ”** 字段

	* 将 **“分母”** 设为 **“Sales | Sales”** 字段

	* 将度量重命名为 **“利润率”**

	![图片 372](Linked_image_Files/PowerBI_Lab04A_image44.png)

	![图片 373](Linked_image_Files/PowerBI_Lab04A_image45.png)

11. 确保选择 **“利润率”** 度量，然后在 **“度量工具”** 上下文功能区中，将格式设置为 **“百分比”**，保留两位小数。

	![图片 374](Linked_image_Files/PowerBI_Lab04A_image46.png)

12. 若要测试这两种度量，请首先选择报表页面上的表视觉对象。

13. 在 **“字段”** 窗格中，检查这两个度量。

	![图片 375](Linked_image_Files/PowerBI_Lab04A_image47.png)

14. 单击并拖动右参考线以拓宽表视觉对象。

	![图片 376](Linked_image_Files/PowerBI_Lab04A_image48.png)

15. 验证这些度量是否生成了格式正确的合理结果。

	![图片 378](Linked_image_Files/PowerBI_Lab04A_image49.png)

### 完成

在此任务中，你将完成实验室。

1. 若要删除表，请通过单击选择表，然后按 **Delete** 键。

2. 保存 Power BI Desktop 文件。

	*在下一个实验室中，你将通过配置多对多关系和行级安全性来增强数据模型*。
