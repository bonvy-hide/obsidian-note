##  一、启动服务

```powershell
# 启动服务
uv run uvicorn main:app --reload
```
## 二、导入模板相关

#### 1、主要指标表
导入数据时要选择的科目，缺一不可，按照单季度为维度，代码会自动处理近十个年度的

![[Pasted image 20260815192558.png]]

示例模板：
![[ygr主要指标.xls]]

也可通过url直接下载：
```
## GET请求，只要替换code
https://basic.10jqka.com.cn/api/stock/export.php?export=diy&type=simple&code=688008&userid=723895634
```

#### 2、资产负债表
直接导出资产负债表，按报告期，只去最新一季度，示例模板：
![[mt资产负债表.xlsx]]

或

![[ygr资产负债表.xls]]

也可通过url直接下载：
```url
## GET请求，只要替换code
https://basic.10jqka.com.cn/api/stock/export.php?export=debt&type=report&code=300750
```

#### 4、市值与业绩表

通过问财提示词模板得到
```

请为【[公司名]】生成可下载的Excel：近十年每季度最后一个交易日的A股不复权收盘价、季度末总股本(万股)、按“收盘价×总股本股÷1亿”计算的总市值(亿元)，以及按累计财报倒算的单季度营业总收入(亿元)。未披露营收留空，不要估算；Excel需包含数据表、公式说明和口径说明，并给出下载链接。
```

示例数据：
![[比亚迪_近十年季度收盘价总股本总市值及单季度营收.xlsx]]

___
[[Pasted image 20260815192558.png|测试别名用法]]

