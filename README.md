![CLEVER DATA GIT REPO](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/0-clever-data-github.png "李聪明的数据库")

# 查找最后几天的查询（Query）
#### Find Last Few Days Of Query
**发布-日期: 2014年04月24日 (评论)**

## Contents

- [中文](#中文)
- [English](#English)
- [SQL Logic](#Logic)
- [Build Info](#Build-Info)
- [Author](#Author)
- [License](#License) 


## 中文
如果你想通过使用DateTime的一种简单的方法来获取最近几天的历史记录，你只需创建几个DateTime变量，并为它们提供今天的日期，或前几天的日期。这样，你就可以查询在逻辑（logic）中最近7天的历史记录。
以下有个简单的例子：


## English
If you ever wanted a simple way to get the last several days history using a DateTime column you can simply create a couple of DateTime Variables, and supply them with todays date, or todays date minus several days. This way you can include the last 7 days in your query logic.

Here’s a quick example:

---
## Logic
```SQL
use MyDatabase
set nocount on
	declare @today datetime 		= ( select getdate() )
	declare @last_7_days datetime 	= ( select getdate() - 7 ) -- today minus 7 days
select
, 	'CreateDate' = convert(char, CreateDate, 9)
, 	'CreateDate' = CreateDate
from
	MyDatabase.MyTable
where
	CreateDate &gt; @last_7_days 
-- include it with a greater than sign in the where clause and you will get the last several days. 
order by
	timestamp asc


```



[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

- **李聪明的数据库 Lee's Clever Data**
- **Mike的数据库宝典 Mikes Database Collection**
- **李聪明的数据库** "Lee Songming"

[![Gist](https://img.shields.io/badge/Gist-李聪明的数据库-<COLOR>.svg)](https://gist.github.com/congmingshuju)
[![Twitter](https://img.shields.io/badge/Twitter-mike的数据库宝典-<COLOR>.svg)](https://twitter.com/mikesdatawork?lang=en)
[![Wordpress](https://img.shields.io/badge/Wordpress-mike的数据库宝典-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)

---
## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Lee Songming](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/1-clever-data-github.png "李聪明的数据库")

