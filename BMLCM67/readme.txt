AntMCM25 数据集说明 / Dataset README

1. 概览 / Overview
AntMCM25 包含膜翅目蚁科的 25 个蚂蚁物种类别。图片按物种目录组织，类别样本数量不均衡，并包含不同背景及部分物种的不同生活阶段图像。
AntMCM25 contains 25 ant species classes within Formicidae, Hymenoptera. Images are organized by species, with imbalanced class sizes, varied backgrounds, and multiple life stages in some species.

2. 数据规模与格式 / Size and Format
类别数 / Classes: 25
JPG 文件数 / JPG files: 13,602
每类文件数 / Files per class: 102-1,802
图片体积 / Image size: 7.77 GB (1 GB = 1,000,000,000 bytes)
文件扩展名 / File extension: .jpg
图像尺寸不统一，读取时应按文件内容识别实际编码格式。
Image dimensions vary. Decode files by their contents rather than relying solely on their extension.

3. 来源 / Source
图像采集来源为全球生物多样性信息机构 GBIF：https://www.gbif.org/ 。Excel 保留类别名称、分类层级及部分生物学描述。网址编码文件名可提供来源线索，但不是完整的逐图作者和许可清单；本包未附统一许可文件。
Images were collected through the Global Biodiversity Information Facility (GBIF): https://www.gbif.org/ . The workbook provides names, taxonomy, and selected biological descriptions. Encoded source URLs in filenames are provenance clues, not a complete per-image attribution/license manifest. No unified license file is supplied.

4. 文件内容 / Files
images/<类别目录 / class folder>/*.jpg
膜翅目Hymenoptera.xlsx: 类别信息表 / class metadata workbook
images.txt: 图片编号与相对路径 / image ID and relative path
image_class_labels.txt: 图片编号与类别编号 / image ID and class ID
readme.txt: 本说明 / this description

5. 编号与标注 / IDs and Annotation
类别编号从 01 连续至 25，目录名保留学名后缀。Excel 的 ID、类别目录和两个 TXT 清单使用相同的 1 起始类别编号。
Class folder prefixes run from 01 to 25, with scientific-name suffixes preserved. Workbook IDs, folders, and TXT manifests share the same one-based class IDs.

images.txt 每行格式 / line format:
image_id class_folder/filename.jpg
image_class_labels.txt 每行格式 / line format:
image_id class_id

图片路径相对于 images/。两个清单中的 image_id 一一对应，编号从 1 连续递增。文件名可能含空格，解析 images.txt 时应只在第一个空白处分隔。
Paths are relative to images/. Image IDs match between the two manifests and start at 1. Filenames may contain spaces; split images.txt lines at the first whitespace only.

Excel 的“整理数量”表示本包该类别的 JPG 文件数，“类别目录”对应实际目录名。其他采集和数量字段保留原整理记录。形态、背景、分布等文字是类别级资料，不是逐张属性标注。
Workbook 整理数量 gives current JPG file counts and 类别目录 gives actual folder names. Other acquisition/count fields retain curation records. Morphology, background, and distribution text describes classes rather than image-level attributes.

6. 完整类别 / Complete Class List
ID	类别目录 / Class folder	中文名 / Chinese name	文件数 / Files
01	01Solenopsis_invicta_Buren	红火蚁	1802
02	02Solenopsis_geminata	热带火蚁	149
03	03Myrmica_rubra	小红蚁	551
04	04Oecophylla_smaragdina	黄猄蚁	1384
05	05Anoplolepis_gracilipes	细足捷蚁	328
06	06Brachymyrmex_patagonicus	巴塔哥尼亚短蚁	336
07	07Camponotus_aethiops	艾提弓背蚁	179
08	08Camponotus_compressus	侧扁弓背蚁	189
09	09Camponotus_habereri	哈氏弓背蚁	102
10	10Camponotus_herculeanus	广布弓背蚁	1379
11	11Camponotus_japonicus	日本弓背蚁	147
12	12Camponotus_nicobarensis	尼科巴弓背蚁	250
13	13Camponotus_piceus	凹背弓背蚁	168
14	14Camponotus_vagus	黑弓背蚁	428
15	15Formica_cunicularia	掘穴蚁	120
16	16Formica_fusca	丝光褐林蚁	857
17	17Formica_pratensis	草地蚁	187
18	18Formica_rufa	红褐林蚁	426
19	19Formica_sanguinea	血红林蚁	409
20	20Lasius_alienus	玉米毛蚁	462
21	21Lasius_emarginatus	凹毛蚁	257
22	22Lasius_flavus	黄毛蚁	976
23	23Lasius_fuliginosus	亮毛蚁	1025
24	24Lasius_niger	黑毛蚁	805
25	25Lasius_umbratus	遮盖毛蚁	686

