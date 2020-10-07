### 实验室 08A

在 Power BI Desktop 中设计报表，第 1 部分

# 概述

**完成实验室预计需要花费 45 分钟**

在本实验室中，你将创建一个三页的报表，名为 **“销售报表”**。然后，你将该报表发布到 Power BI，随后打开并与之交互。

在本实验室中，你将学习如何：

* 使用 Power BI Desktop 创建实时连接

* 设计报表

* 配置视觉对象字段和格式属性

# 练习 1 ：创建报表

在本练习中，你将创建一个三页的报表，名为 **“销售报表”**。

### 任务 1：创建新的文件

在此任务中，你将创建与 **Sales Analysis** 数据集的实时连接。

1. 要打开 Power BI Desktop，请在任务栏上单击 Microsoft Power BI Desktop 快捷方式。

	![图片 2](Linked_image_Files/PowerBI_Lab08A_image1.png)

2. 在欢迎屏幕的右上角，单击 **X**。

	![图片 1](Linked_image_Files/PowerBI_Lab08A_image2.png)

3. 单击 **“文件”** 功能区选项卡以打开后台视图，然后选择 **“保存”**。

	![图片 13](Linked_image_Files/PowerBI_Lab08A_image3.png)

4. 在**另存为**窗口中，导航到 **“D:\DA100\MySolution”** 文件夹。

5. 在 **“文件名称”** 框中，输入 **“销售报表”**。

	![图片 14](Linked_image_Files/PowerBI_Lab08A_image4.png)

6. 单击 **“保存”**。

	![图片 17](Linked_image_Files/PowerBI_Lab08A_image5.png)

### 任务 2：创建实时连接

在此任务中，你将创建与 **Sales Analysis** 数据集的实时连接。

1. 要创建实时连接，在 **“主页”** 功能区选项中的 **“数据”** 组内，单击 **“获取数据”**, 向下箭头，然后选择 **“Power BI 数据集”**。

	![图片 6](Linked_image_Files/PowerBI_Lab08A_image6.png)

2. 在 **“选择创建报表所需的数据集”** 窗口中，选择 **“销售分析”** 数据集。

	![图片 7](Linked_image_Files/PowerBI_Lab08A_image7.png)

3. 单击 **“创建”**。

	![图片 9](Linked_image_Files/PowerBI_Lab08A_image8.png)

4. 在右下角的状态栏中，请注意已建立实时连接。

5. 在 **“字段”** 窗格中，请注意已列出数据模型表。

	*Power BI Desktop 不能再用于开发数据模型；在实时连接模式下，它只是一个报表创作工具。但是，它可以创建度量值，不过这些度量值仅在报表中可用。你不会在此实验室中添加任何报告范围的度量值*。

6. 保存 Power BI Desktop 文件。

	*回想一下，你在 **“实验室 05A”** 的模型中添加了 **“Salespeople”** 角色 。由于你是 Power BI 数据集的所有者，因此不会强制执行角色。这就解释了为什么在这个实验室中，你可以看到所有数据*。

	*当你与数据集的非所有者共享报表和仪表板时，必须将其帐户（或他们所属的安全组）映射到 **“销售人员”** 角色。在实**验室 12A**中共享内容之前，你将配置此项*。

### 任务 3：设计第 1 页

在此任务中将设计第一个报表页面。完成设计后，页面将如下所示：  
	![图片 40](Linked_image_Files/PowerBI_Lab08A_image9.png)

1. 要重命名页面，请在左下角右键单击 **“第 1 页”**，然后选择 **“重命名”**。

	![图片 36](Linked_image_Files/PowerBI_Lab08A_image10.png)

	*提示：你也可以双击页面名称*。

2. 将页面重命名为 **“概述”**，然后按 **Enter**。

	![图片 37](Linked_image_Files/PowerBI_Lab08A_image11.png)

3. 要添加图片，请在 **“插入”** 功能区选项卡，从 **“元素”** 组里面，单击 **“图片”**。

	![图片 10](Linked_image_Files/PowerBI_Lab08A_image12.png)

4. 在 **“打开”** 窗口中，导航到 **“D:\DA100\Data”** 文件夹。

5. 选择 **“AdventureWorksLogo.jpg”** 文件，然后单击 **“打开”**。

	![图片 11](Linked_image_Files/PowerBI_Lab08A_image13.png)

6. 拖动图像以将其重新放置在左上角，并拖动引导标记以调整其大小。

	![图片 12](Linked_image_Files/PowerBI_Lab08A_image14.png)

7. 要添加切片器，请先通过单击报表页面的空白区域来取消选择图像。

8. 在 **“字段”** 窗格中，选择 **“日期”** | **“年”** 字段（不是 **“年”** 层次级别）。

9. 请注意，年份值表已添加到报表页面。

10. 要将视觉对象从表格转换为切片器，请在 **“可视化”** 窗格中，选择 **“切片器”**。

	![图片 15](Linked_image_Files/PowerBI_Lab08A_image15.png)

11. 要将切片器从列表转换为下拉列表，请在切片器的右上角，单击向下箭头，然后选择 **“下拉”**。

	![图片 18](Linked_image_Files/PowerBI_Lab08A_image16.png)

12. 调整切片器的大小并重新放置，使其位于图像下方，从而使宽度与图像相同。

	![图片 19](Linked_image_Files/PowerBI_Lab08A_image17.png)

13. 在 **“年”** 切片器，选择 **“2020财年”**，然后折叠下拉列表。

	![图片 20](Linked_image_Files/PowerBI_Lab08A_image18.png)

	报表页面现在按 **“FY2020”** 筛选。

14. 通过单击报表页面的空白区域来取消选择切片器。

15. 基于 **“区域”** 创建第二个切片器 | **“区域”** 字段（不是**区域**层级）。

16. 将切片器保留为列表，然后调整切片器的大小并将其重新放置在 **“年份”** 切片器下。

	![图片 21](Linked_image_Files/PowerBI_Lab08A_image19.png)

17. 要格式化切片器，请在 **“可视化”** 窗格中，打开 **“格式”** 窗格。

	![图片 22](Linked_image_Files/PowerBI_Lab08A_image20.png)

18. 然后展开 **“选择控件”** 组。

	![图片 23](Linked_image_Files/PowerBI_Lab08A_image21.png)

19. 将 **“显示‘全选’选项”** 设置为 **“启用”**。

	![图片 24](Linked_image_Files/PowerBI_Lab08A_image22.png)

20. 在 **“区域”** 切片器中，请注意第一个项目现在是 **“全选”**。

	*选中后，此项目将全选或取消选择所有项目。它使报表用户更容易设置正确的筛选器*。

21. 通过单击报表页面的空白区域来取消选择切片器。

22. 要向页面添加图表，请在 **“可视化”** 窗格中，单击 **“折线图和堆积柱形图”** 视觉对象类型。

	![图片 25](Linked_image_Files/PowerBI_Lab08A_image23.png)

23. 调整视觉对象的大小和位置，使其位于徽标的右侧，从而填充报表页面的宽度。

	![图片 26](Linked_image_Files/PowerBI_Lab08A_image24.png)

24. 将以下字段拖到视觉对象中：

	*  Date | Month

	* Sales | Sales

25. 请注意，在视觉对象字段窗格（不是 **“字段”** 窗格 - 视觉对象字段窗格位于 **“可视化”** 窗格下方）中，这些字段已分配给 **“共享轴”** 和 **“列值”** 井。

	![图片 27](Linked_image_Files/PowerBI_Lab08A_image25.png)

	*将视觉对象拖到视觉文件中即可将其添加到默认井中。为了精确起见，你可以像现在一样将字段直接拖到井中*。

26. 从 **“字段”** 窗格中，拖动 **“销售额”** | **“Profit Margin”** 字段拖动到折线图下的 **“值”** 井。

	![图片 28](Linked_image_Files/PowerBI_Lab08A_image26.png)

27. 请注意，该视觉对象只有 11 个月份。

	*尚未提供上月（即 2020 年 6 月）的任何销售数据。该视觉对象默认消除了销售数据为“空白”的月份。现在，你将配置视觉对象以显示所有月份*。

28. 在视觉对象字段窗格中的 **“共享轴”** 井中，对于 **“月份”** 字段，单击向下箭头，然后选择 **“显示无数据的项目”**。

	![图片 29](Linked_image_Files/PowerBI_Lab08A_image27.png)

29. 请注意，现在显示月份 **“2020 June”**。

30. 通过单击报表页面的空白区域来取消选择图表。

31. 要向页面添加图表，请在 **“可视化”** 窗格中，单击 **“地图”** 视觉对象类型。

	![图片 32](Linked_image_Files/PowerBI_Lab08A_image28.png)

32. 调整该视觉对象的大小和位置，使之位于柱形图/折线图之下，占据报表页面宽度的一半。

	![图片 33](Linked_image_Files/PowerBI_Lab08A_image29.png)

33. 将以下字段添加到视觉对象井中：

	* 位置： **Region | Country**

	* 图例：**Product | Category**

	* 大小： **Sales | Sales**

34. 通过单击报表页面的空白区域来取消选择图表。

35. 要向页面添加图表，请在 **“可视化”** 窗格中，单击 **“堆积条形图”** 视觉对象类型。

	![图片 34](Linked_image_Files/PowerBI_Lab08A_image30.png)

36. 调整该视觉对象的大小和位置，使之填充报表页面的剩余空间。

	![图片 35](Linked_image_Files/PowerBI_Lab08A_image31.png)

37. 将以下字段添加到视觉对象井中：

	* 轴：**Product | Category**

	* 值：**Sales | Quantity**

38. 要设置视觉对象的格式，请打开 **“格式”** 窗格。

	![图片 38](Linked_image_Files/PowerBI_Lab08A_image32.png)

39. 展开 **“数据颜色”** 组，然后将 **“默认颜色”** 属性设置为合适的颜色（与柱形图/折线图相反）。

40. 将 **“数据标签”** 属性设置为 **“启用”**。

	![图片 39](Linked_image_Files/PowerBI_Lab08A_image33.png)

41. 保存 Power BI Desktop 文件。

	*第一页的设计现已完成*。

  
 

### 任务 4：设计第 2 页

在此任务中，你将设计报表的第 2 页。完成设计后，页面将如下所示：

![图片 41](Linked_image_Files/PowerBI_Lab08A_image34.png)

*由于实验室中已提供了详细说明，因此，实验室步骤将提供更简洁的说明。如果需要详细说明，可以参考其他任务*。

1. 要创建新页面，请单击左下角的加号图标。

	![图片 42](Linked_image_Files/PowerBI_Lab08A_image35.png)

2. 将页面重命名为 **“Profit”**。

	![图片 43](Linked_image_Files/PowerBI_Lab08A_image36.png)

3. 根据 **“Region | Region”** 字段添加切片器。

4. 使用 **“格式”** 窗格启用“全选”选项（在 **“选择控件”** 组中）。

5. 调整该切片器的大小和位置，使之位于报表页面的左侧，大约占页面高度的一半。

	![图片 44](Linked_image_Files/PowerBI_Lab08A_image37.png)

6. 添加矩阵视觉对象，并调整大小和位置，使之填充报表页面的剩余空间

	![图片 45](Linked_image_Files/PowerBI_Lab08A_image38.png)

7. 将 **“Date | Fiscal”** 层次结构添加到“矩阵”视觉对象的 **“行”** 井。

	![图片 46](Linked_image_Files/PowerBI_Lab08A_image39.png)

8. 添加以下五笔 **“销售”** 表字段至 **“值”** 井：

	* Orders（来自 **“Counts”** 文件夹）

	* Sales

	* Cost

	* Profit

	* Profit Margin

	![图片 3](Linked_image_Files/PowerBI_Lab08A_image40.png)

9. 在 **“筛选器”** 窗格（位于 **“可视化”** 窗格左侧）中，请注意 **“此页上的筛选器”** 井（你可能需要向下滚动）。

	![图片 57](Linked_image_Files/PowerBI_Lab08A_image41.png)

10. 从 **“字段”** 窗格中，将 **“Product | Category”** 字段拖动到 **“此页上的筛选器”** 井。

11. 在筛选器卡的右上角，单击箭头以折叠筛选器卡。

	![图片 58](Linked_image_Files/PowerBI_Lab08A_image42.png)

	*已添加到 **“筛选器”** 窗格的字段可以实现与切片器相同的结果。区别之一是它们不占用报告页面上的空间。另一个区别是可以针对更高级的筛选要求进行配置*。

12. 将以下每个 **“Product”** 表字段添加到 **“此页上的筛选器”** 井，并将其直接折叠在 **“类别”** 卡下：

	* Subcategory

	* Product

	* Color

	![图片 60](Linked_image_Files/PowerBI_Lab08A_image43.png)

13. 要折叠 **“筛选器”** 窗格，请在窗格的右上方，单击箭头。

	![图片 68](Linked_image_Files/PowerBI_Lab08A_image44.png)

14. 保存 Power BI Desktop 文件。

	第二页的设计现已完成。

### 任务 5：设计第 3 页

在此任务中，你将设计第 3 页，也就是报表的最后一页。完成设计后，页面将如下所示：  
	![图片 69](Linked_image_Files/PowerBI_Lab08A_image45.png)

1. 创建一个新页面，然后将其重命名为 **“My Performance”**。

	*回想一下，行级别安全性已配置为确保用户仅能查看其销售区域和目标的数据。将此报表分发给销售人员后，他们将只会看到自己的销售业绩结果*。

2. 要在报表设计和测试过程中模拟行级安全筛选器，请将 **“Salesperson (Performance) | Salesperson”** 字段添加到 **“筛选器”** 窗格上的 **“此页上的筛选器”** 井内。

3. 在筛选器卡中，向下滚动销售员列表，然后查看 **“Michael Blythe”**。

	![图片 73](Linked_image_Files/PowerBI_Lab08A_image46.png)

	*在实**验室 12A**的应用中分发报表之前，系统将指示你删除此筛选器*。

4. 根据 **“Date | Year”** 字段添加下拉切片器，然后调整大小和位置，使之位于页面的左上角。

	![图片 70](Linked_image_Files/PowerBI_Lab08A_image47.png)

5. 在切片器中，选择 **FY2019**。

	![图片 71](Linked_image_Files/PowerBI_Lab08A_image48.png)

6. 添加一个 **“多行卡”** 视觉对象，然后调整其大小和位置，使其位于切片器的右侧并填充页面的剩余宽度。

	![图片 72](Linked_image_Files/PowerBI_Lab08A_image49.png)

	![图片 74](Linked_image_Files/PowerBI_Lab08A_image50.png)

7. 将以下四个字段添加到该视觉对象：

	* Sales | Sales

	* Targets | Target

	* Targets | Variance

	* Targets | Variance Margin

8. 设置视觉对象格式：

	* 在 **“数据标签”** 组中，将 **“文本大小”** 属性增加到 **“28 磅”**

	* 在 **“背景”** 组中，将 **“颜色”** 设置为浅灰色

	![图片 79](Linked_image_Files/PowerBI_Lab08A_image51.png)

9. 添加一个 **“簇状条形图”** 视觉对象，然后调整其大小和位置，使其位于多行卡视觉对象的下方，并填充页面的剩余高度，达到多行卡视觉对象宽度的一半。

	![图片 77](Linked_image_Files/PowerBI_Lab08A_image52.png)

	![图片 78](Linked_image_Files/PowerBI_Lab08A_image53.png)

10. 将以下字段添加到视觉对象井中：

	* 轴：**Date | Month**

	* 值：**“Sales | Sales”** 和 **“Targets | Target”**

	![图片 80](Linked_image_Files/PowerBI_Lab08A_image54.png)

11. 要创建视觉对象的副本，请按 **“Ctrl+C”**，然后按 **“Ctrl+V”**。

12. 将复制的视觉对象放在原始视觉对象的右侧。

	![图片 82](Linked_image_Files/PowerBI_Lab08A_image55.png)

13. 要修改可视化效果类型，请在 **“可视化效果”** 窗格中，选择 **“簇状柱形图”**。

	![图片 81](Linked_image_Files/PowerBI_Lab08A_image56.png)

	*现在可以看到由两种不同的可视化类型表示的相同数据。这不是页面布局的好用法，但是你将在实**验室 09A** 中通过叠加视觉对象来改进页面布局。通过向页面添加按钮，你将允许报表用户确定两个视觉对象中的哪个可见*。

	*第三页和最后一页的设计现已完成*。

### 任务 6：发布报表

在此任务中，你将发布报表。

1. 选择 **“总览”** 页面。

2. 保存 Power BI Desktop 文件。

3. 在 **“主页”** 功能区选项卡上的 **“共享”** 组中，单击 **“发布”**。

	![图片 64](Linked_image_Files/PowerBI_Lab08A_image57.png)

4. 将报表发布到 **“销售分析”** 工作区。

5. 保持 Power BI Desktop 打开状态。

	*在下一个练习中，你将在 Power BI 服务中浏览报表*。

# 练习 2：浏览报表

在本练习中，将在 Power BI 服务中浏览 **“销售报表”**。

### 任务 1：浏览报表

在此任务中，你将在 Power BI 服务中浏览 **“Sales Report”**。

1. 在 Edge 的 Power BI 服务中，在 **“导航”** 窗格查看 **“销售分析”** 工作区的内容，然后单击 **“销售报表”** 报表。

	![图片 83](Linked_image_Files/PowerBI_Lab08A_image58.png)

	*报表发布操作已将报表添加到你的工作区。如果看不到该工作区，请按 **F5** 重新加载浏览器，然后再次展开该工作区*。

2. 在 **“区域”** 切片器中，按下 **Ctrl** 键的同时选择多个区域。

3. 在柱形图/折线图中，选择任何月份对应的柱形以对页面进行交叉筛选。

4. 按下 **Ctrl** 键的同时再选择一个月份。

	*默认情况下，交叉筛选会筛选页面上的其他视觉对象*。

5. 请注意，条形图已筛选并突出显示，条形的粗体部分代表筛选后的月份。

6. 将光标悬停在视觉对象上，然后单击右上角的筛选器图标。

	![图片 88](Linked_image_Files/PowerBI_Lab08A_image59.png)

	*筛选器图标可让你了解应用于视觉对象的所有筛选器，包括切片器和其他视觉对象的交叉筛选器*。

7. 将光标悬停在条形上，然后注意工具提示信息。

8. 要撤消交叉筛选器，请在柱形图/折线图中单击视觉对象的空白区域。

9. 将光标指针悬停在映射视觉对象上方，然后单击右上角的**焦点**图标。

	![图片 85](Linked_image_Files/PowerBI_Lab08A_image60.png)

	*在焦点模式下，将视觉对象缩放到整个页面大小*。

10. 将光标悬停在饼图的不同部分上以显示工具提示。

11. 要返回报表页面，请单击左上角的 **“返回到报表”**。

	![图片 86](Linked_image_Files/PowerBI_Lab08A_image61.png)

12. 再次将光标悬停在地图视觉对象上方，然后单击省略号 (…)，并注意菜单选项。

	![图片 87](Linked_image_Files/PowerBI_Lab08A_image62.png)

13. 尝试每个选项。

14. 在左侧的 **“页面”** 窗格中，选择 **Profit** 页面。

	![图片 84](Linked_image_Files/PowerBI_Lab08A_image63.png)

15. 请注意 **“Region”** 切片器的选项与“总览”页面上的 **“Region”** 切片器不同。  
	*切片器未同步。在下一个实验室中，你将修改报表设计，以确保它们在页面之间同步*。

16. 在 **“筛选器”** 窗格（位于右侧）中，展开筛选器卡，然后应用一些筛选器。      
***“筛选器”** 窗格允许你以切片器的形式在一个页面上定义页面原本不可能容纳的更多筛选器*。

17. 在矩阵视觉对象中，使用加号 (+) 按钮展开到 **Fiscal** 层次结构。

18. 选择 **“我的业绩”** 页面。  
	![图片 89](Linked_image_Files/PowerBI_Lab08A_image64.png)

19. 在菜单栏右上角单击“查看”，然后选择“全屏”。  
	![图片 90](Linked_image_Files/PowerBI_Lab08A_image65.png)

20. 通过修改切片器与页面进行交互，并对页面进行交叉筛选。

21. 在左下角，请注意用于更改页面、在页面之间向后或向前导航或退出全屏模式的命令。

22. 退出全屏模式。  
	![图片 91](Linked_image_Files/PowerBI_Lab08A_image66.png)

23. 要返回工作区，请在 Breadcrumb 结尾中单击你的工作区名称。  
	![图片 92](Linked_image_Files/PowerBI_Lab08A_image67.png)

24. 使 Edge 浏览器窗口保持打开状态。  
	*你将通过实**验室 09A** 中的高级功能来增强报表设计*。
