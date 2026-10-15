BMLCM67 数据集说明 / Dataset README

1. 概览 / Overview
BMLCM67 包含鳞翅目的 67 个蝶蛾物种类别。图片按物种目录组织，类别样本数量不均衡，并包含不同背景及部分物种的不同生活阶段图像。
BMLCM67 contains 67 butterfly and moth species classes within Lepidoptera. Images are organized by species, with imbalanced class sizes, varied backgrounds, and multiple life stages in some species.

2. 数据规模与格式 / Size and Format
类别数 / Classes: 67
JPG 文件数 / JPG files: 66,420
每类文件数 / Files per class: 16-4,332
图片体积 / Image size: 18.96 GB (1 GB = 1,000,000,000 bytes)
文件扩展名 / File extension: .jpg
图像尺寸不统一，读取时应按文件内容识别实际编码格式。
Image dimensions vary. Decode files by their contents rather than relying solely on their extension.

3. 来源 / Source
图像采集来源为全球生物多样性信息机构 GBIF：https://www.gbif.org/ 。Excel 保留类别名称、分类层级及部分生物学描述。网址编码文件名可提供来源线索，但不是完整的逐图作者和许可清单；本包未附统一许可文件。
Images were collected through the Global Biodiversity Information Facility (GBIF): https://www.gbif.org/ . The workbook provides names, taxonomy, and selected biological descriptions. Encoded source URLs in filenames are provenance clues, not a complete per-image attribution/license manifest. No unified license file is supplied.

4. 文件内容 / Files
images/<类别目录 / class folder>/*.jpg
鳞翅目Lepidoptera.xlsx: 类别信息表 / class metadata workbook
images.txt: 图片编号与相对路径 / image ID and relative path
image_class_labels.txt: 图片编号与类别编号 / image ID and class ID
readme.txt: 本说明 / this description

5. 编号与标注 / IDs and Annotation
类别编号从 01 连续至 67，目录名保留学名后缀。Excel 的 ID、类别目录和两个 TXT 清单使用相同的 1 起始类别编号。
Class folder prefixes run from 01 to 67, with scientific-name suffixes preserved. Workbook IDs, folders, and TXT manifests share the same one-based class IDs.

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
01	01Papilio_paris	巴黎翠凤蝶	741
02	02Papilio_Xuthus	柑橘凤蝶	609
03	03Pachliopta_aristolochiae	红珠凤蝶	1199
04	04Troides_helena	裳凤蝶	2293
05	05Troides aeacus	金裳凤蝶	822
06	06Acytolepis_puspa	钮灰蝶	1156
07	07Taraka_hamada_Druce	蚜灰蝶	257
08	08Curetis_acuta_Moore	尖翅银灰蝶	539
09	09Tajuria_cippus	双尾灰蝶	488
10	10Argynnis_adippe	灿福蛱蝶	1342
11	11Argynnis_hyperbius	斐豹蛱蝶	1556
12	12Kaniska_canace	琉璃蛱蝶	654
13	13Phaedyma_columella	柱菲蛱蝶	350
14	14Delias_pasithoe	报喜斑粉蝶	795
15	15Hebomoia_glaucippe	鹤顶粉蝶	486
16	16Pieris_canidia	东方菜粉蝶	809
17	17Mycalesis_gotama_Moore	稻眼蝶	315
18	18Melanitis_leda_Linnaeus	稻褐眼蝶	3012
19	19Bibasis_gomata	白伞弄蝶	230
20	20Hasora_chromus	双斑趾弄蝶	728
21	21Hasora_schoenherr	金带趾弄蝶	153
22	22Choaspes_benjaminii	尖翅弄蝶	209
23	23Iambrix_salsala	雅弄蝶	544
24	24Pyrgus_alveus_Hübner	北方花弄蝶	647
25	25Parnara_guttata_Bremer_et_Grey	稻苞虫	452
26	26Parnara_bada	幺纹稻弄蝶	397
27	27Actias_ningpoana	绿尾天蚕蛾	550
28	28Acherontia_lachesis	鬼脸天蛾	529
29	29Acherontia_atropos	赭带鬼脸天蛾	2061
30	30Daphnis_nerii	夹竹桃天蛾	847
31	31Daphnis_hypo_hous_Cramer	茜草白腰天蛾	292
32	32Theretra_oldenlandiae	凤仙花天蛾	618
33	33Milionia_basalis	橙带蓝尺蛾	2039
34	34Amerila_astreus	闪光玫灯蛾	451
35	35Areas_galactina	乳白格灯蛾	430
36	36Creatonotos_gangis	黑条灰灯蛾	635
37	37Cyana_hamata	优雪苔蛾	2174
38	38Cyana_sanguinea	血红雪苔蛾	90
39	39Nyctemera_adversata	粉蝶灯蛾	1988
40	40Nyctemera_carissima_Swinhoe	角蝶灯蛾	297
41	41Nyctemera_lacticinia_Cramer	蝶灯蛾	493
42	42Hyphantria_cunea	美国白蛾	2733
43	43Catocala_fraxini	缟裳夜蛾	1970
44	44Eligma_narcissus	旋夜蛾	247
45	45Spodoptera_exigua	甜菜夜蛾	1137
46	46Spodoptera_litura_Fabricius	斜纹夜蛾	1693
47	47Spodoptera_frugiperda_(Smith)	草地贪夜蛾	1255
48	48Agrotis_ipsilon	小地老虎	4332
49	49Agrotis_segetum	黄地老虎	3694
50	50Naranga_aenescens_Moore	稻螟蛉	23
51	51Athetis_lepigone	二点委夜蛾	663
52	52Mamestra_brassicae	甘蓝夜蛾	2247
53	53Chlumetia_transversa	芒果横线尾夜蛾	71
54	54Mythimna_separata	黏虫	155
55	55Adris_tyrannus_Guenée	枯叶夜蛾	117
56	56Helicoverpa_armigera	棉铃虫 	2303
57	57Leucania_loreyi_duponchel	劳氏粘虫	289
58	58Trachea_atriplicis_Linnaeus	陌夜蛾	2675
59	59Chilo_suppressalis(Walker)	二化螟	16
60	60Scirpophaga_incertulas_Walker	三化螟	50
61	61Circobotys_aurealis	金黄镰翅野螟 	100
62	62Ostrinia_nubilalis	玉米螟	1910
63	63Cnaphalocrocis_medinalis_Guenée	稻纵卷叶螟	662
64	64Conogethes_punctiferalis	桃蛀螟	173
65	65Plutella_xylostella	小菜蛾	1388
66	66Cydia_pomonella(L.)	苹果蠹蛾	2188
67	67Tuta_absoluta	番茄潜叶蛾	52
