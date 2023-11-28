---
id: "aspose-diagram-for-net-18-10-release-notes"
slug: "aspose-diagram-for-net-18-10-release-notes"
linktitle: "Aspose.Diagram for .NET 18.10 Примечания к выпуску"
title: "Aspose.Diagram for .NET 18.10 Примечания к выпуску"
weight: 30
description: "Aspose.Diagram for .NET 18.10 Примечания к выпуску – the latest updates and fixes."
type: "repository"
layout: "release"
---
{{% alert color="primary" %}} 

 Эта страница содержит примечания к выпуску для[Aspose.Diagram for .NET 18.10](https://www.nuget.org/packages/Aspose.Diagram/18.10.0).

{{% /alert %}} 
## **Улучшения и изменения**

|**Ключ**|**Резюме**|**Категория**|
|:- |:- |:- |
|DIAGRAMNET-51527|Изображения теряются после преобразования VSDM в SVG|Улучшение|
|DIAGRAMNET-51532|От VSD до PDF — неверная тень изображения|Улучшение|
|DIAGRAMNET-51536|Тень формы была удалена после преобразования VSDX в SVG.|Улучшение|
|DIAGRAMNET-51544|Подчеркивание удаляется из текста после преобразования VSDM в SVG.|Улучшение|
|DIAGRAMNET-51558|Реализовать геттер для Shape.ConnectorsType|Улучшение|
|DIAGRAMNET-51520|От VDX до HTML — в выводе появляются дополнительные строки|Ошибка|
|DIAGRAMNET-51521|Шрифт в diagram получает изменения после сохранения VSD как VSDX|Ошибка|
|DIAGRAMNET-51523|с VSDX по SVG - отсутствуют наконечники стрелок|Ошибка|
|DIAGRAMNET-51524|От VSDM до SVG — в выходном файле появились синие кресты.|Ошибка|
|DIAGRAMNET-51525|Форма решения изменяется с ромба на квадрат при преобразовании VSDM в SVG.|Ошибка|
|DIAGRAMNET-51528|Форма решения изменяется с ромба на квадрат при преобразовании VSDM в SVG.|Ошибка|
|DIAGRAMNET-51529|От VSDM до SVG — пунктирные линии преобразованы в заполненные.|Ошибка|
|DIAGRAMNET-51531|Фигуры смещаются вправо после преобразования VSDX в SVG.|Ошибка|
|DIAGRAMNET-51533|Красные кресты появились после конвертации VISIO в SVG|Ошибка|
|DIAGRAMNET-51534|Красная точка появилась в нижнем левом углу фигуры|Ошибка|
|DIAGRAMNET-51538|Картинки теряются после преобразования VSDX в PDF|Ошибка|
|DIAGRAMNET-51541|Текст становится невидимым после преобразования VSDX в SVG|Ошибка|
|DIAGRAMNET-51542|Текст был удален после преобразования VSDX в SVG|Ошибка|
|DIAGRAMNET-51543|Формат времени и даты изменен после VSDM НА SVG|Ошибка|
|DIAGRAMNET-51545|От VSDX до SVG — текст переносится на вывод|Ошибка|
|DIAGRAMNET-51546|От VSDX до SVG — текст переносится на вывод|Ошибка|
|DIAGRAMNET-51547|От VSDX до SVG — текст переносится на вывод|Ошибка|
|DIAGRAMNET-51548|От VSDX до SVG — текст переносится на вывод|Ошибка|
|DIAGRAMNET-51551|Не удалось получить правильный цвет темы фигур|Ошибка|
|DIAGRAMNET-51552|Перевернутые стрелки показаны в преобразовании SVG.|Ошибка|
|DIAGRAMNET-51559|Проблема с изменением размера текста при преобразовании VSDM в SVG|Ошибка|
|DIAGRAMNET-51560|Соединительные линии становятся тонкими после преобразования в SVG|Ошибка|
## **Public API и обратно несовместимые изменения**
Ниже приведен список любых изменений, внесенных в общедоступный номер API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые с предыдущими изменениями, внесенные в номер Aspose.Diagram for .NET. Если у вас есть сомнения по поводу каких-либо перечисленных изменений, сообщите о них в в[Aspose.Diagram форум поддержки](https://forum.aspose.com/c/diagram/17).
#### **Добавлен InheritLine в форму**
Содержит значения форматирования строки для фигуры, наследуемой родительским стилем и основной фигурой.

{{< highlight "java" >}}

 		Line line = shape.InheritLine;

{{< /highlight >}}


#### **Добавлен GetConnectorsType в форму**
Получить тип соединителей

{{< highlight "java" >}}

 Shapes.GetShape(1).GetConnectorsType()

{{< /highlight >}}
