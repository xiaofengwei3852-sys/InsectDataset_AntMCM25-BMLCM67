# 昆虫物种图像数据集 / Insect Species Image Dataset

## 数据集概览 / Overview

本数据集包含蚂蚁和蝶蛾两部分，共 **99 个类别、82,843 个图片文件**。图片按物种类别存放，每部分附一份 Excel 类别信息表，记录中文名、学名、分类层级及部分生物学描述。

* **蚂蚁数据 `mcmdata`**：31 个类别，属于膜翅目蚁科，包含火蚁、弓背蚁、毛蚁等。
* **蝶蛾数据 `lcmdata`**：68 个类别，属于鳞翅目，包含凤蝶、灰蝶、弄蝶、天蛾、夜蛾等。

具体昆虫数据可以从excel内查看

The dataset contains **99 classes and 82,843 image files** across two collections: ants (`mcmdata`, 31 classes within Formicidae, Hymenoptera) and butterflies/moths (`lcmdata`, 68 classes within Lepidoptera). Images are organized by species. Each collection includes an Excel workbook with Chinese names, scientific names, taxonomic fields, and selected biological descriptions.

You can check the specific insect data in Excel.

## 数据规模 / Dataset Statistics

|数据目录 / Collection|类别数 / Classes|图片文件数 / Image files|图片体积 / Image size|
|-|-:|-:|-:|
|`mcmdata/images`|31|14,054|7.84 GB|
|`lcmdata/images`|68|68,789|19.70 GB|
|合计 / Total|99|82,843|27.54 GB|

类别数量以实际图片目录为准；图片数量按 `.jpg` 扩展名统计。体积仅计图片文件，采用十进制单位（1 GB = 1,000,000,000 bytes）。

各类别的文件数量不均衡：蚂蚁每类 34–1,802 个，蝶蛾每类 16–4,332 个。整理表记录的图片背景包括自然环境和标本背景，部分物种涉及不同生活阶段。

Class counts reflect actual image folders. Image counts include files with a `.jpg` extension. Sizes cover image files only and use decimal GB. Class sizes range from 34 to 1,802 files for ants and from 16 to 4,332 for butterflies/moths. Workbook descriptions mention natural and specimen backgrounds and multiple life stages for some species.

## 目录结构 / Directory Structure

主要数据文件如下。`...` 表示省略的其他类别目录。

The main data files are organized as follows. `...` represents additional class folders.

```text
data\\\_upload/
├── README.md
├── mcmdata/
│   ├── 膜翅目.xlsx
│   └── images/
│       ├── 01Solenopsis\\\_invicta\\\_Buren/
│       │   └── \\\*.jpg
│       ├── 02Solenopsis\\\_fugax/
│       ├── ...
│       └── 31Lepisiota\\\_capensis/
└── lcmdata/
    ├── 鳞翅目.xlsx
    └── images/
        ├── 01Papilio\\\_paris/
        │   └── \\\*.jpg
        ├── 02Papilio\\\_Xuthus/
        ├── ...
        └── 74Tuta\\\_absoluta/
```

每个物种目录内存放该类别的图片。目录名由原整理编号和物种名称组成，保留空格、下划线、括号及 Unicode 字符。图片文件名沿用原始命名，部分含网址的编码片段。

Each species folder contains its class images. Folder names combine a curation ID and a species name, preserving spaces, underscores, parentheses, and Unicode characters. Image filenames retain their existing names; some contain encoded URL fragments.

## 类别信息与标注 / Class Metadata and Labels

### Excel 信息表 / Excel Workbooks

两份工作簿的数据均位于 `Sheet1`。

Both workbooks store their class records in `Sheet1`.

|文件 / File|内容 / Contents|
|-|-|
|`mcmdata/膜翅目.xlsx`|蚂蚁类别信息，31 条记录 / Ant metadata, 31 records|
|`lcmdata/鳞翅目.xlsx`|蝶蛾类别信息，69 条记录 / Butterfly and moth metadata, 69 records|

主要字段如下，具体内容与完整程度因类别而异。

Main metadata fields are listed below. Availability varies by class.

|字段 / Fields|说明 / Description|
|-|-|
|`ID`、`中文名`、`拉丁文`|原整理编号、中文名及学名 / Curation ID, Chinese name, and scientific name|
|`目`、`亚目`、`总科`、`科`、`亚科`、`属`|分类层级 / Taxonomic hierarchy|
|`网页图片数量`、`已爬数量`、`整理数量`|图片采集与整理数量记录 / Image acquisition and curation counts|
|`备注`、`特征`、`分布`等 / Other descriptive fields|部分类别的形态、背景、分布和生物学描述 / Selected morphology, background, distribution, and biological descriptions|

鳞翅目表中的编号 13“绿豹蛱蝶”没有对应的图片目录，因此表内记录数与已提供图片的类别数不同。Excel 数量字段保留整理记录，当前文件数量见上方统计表。空白单元格表示该字段未填写。

The Lepidoptera workbook includes record 13, 绿豹蛱蝶, with no corresponding image folder. Its record count therefore differs from the number of supplied image classes. Workbook count fields retain curation records; the statistics above describe the current files. Blank cells indicate unfilled fields.

### 标签与类别示例 / Labels and Example Classes

图片所在的父目录表示其类别。可通过目录名开头的编号与 Excel 的 `ID` 对应，查询该类别的名称及描述。整理表中的特征、生活阶段等信息属于类别层面，未逐张对应到所有图片。

An image's parent folder identifies its class. Match the folder's numeric prefix to the workbook `ID` to retrieve names and descriptions. Morphology, life-stage, and other descriptive information is class-level metadata rather than attributes assigned to every image.

|数据目录 / Collection|中文名 / Chinese name|整理表学名 / Scientific name|图片文件数 / Files|
|-|-|-|-:|
|`mcmdata`|红火蚁|Solenopsis invicta Buren|1,802|
|`mcmdata`|广布弓背蚁|Camponotus herculeanus|1,379|
|`mcmdata`|黑毛蚁|Lasius niger|805|
|`lcmdata`|巴黎翠凤蝶|Papilio paris|741|
|`lcmdata`|小地老虎|Agrotis ipsilon|4,332|
|`lcmdata`|二化螟|Chilo suppressalis(Walker)|16|

完整类别请查看各 `images` 目录及对应 Excel。

For the complete class inventory, consult each `images` directory and its workbook.

## 

