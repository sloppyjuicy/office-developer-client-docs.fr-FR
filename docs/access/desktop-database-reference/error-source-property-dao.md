---
title: Error.Source, propriété (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 79c5fa1e01bbb6bce4f2cef705f23f3259bf0678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293440"
---
# <a name="errorsource-property-dao"></a>Error.Source, propriété (DAO)


**S’applique à** : Access 2013, Office 2013


Renvoie le nom de l'objet ou de l'application à l'origine de l'erreur.

## <a name="syntax"></a>Syntaxe

*.* Source

*expression* Variable qui représente un objet **Error.**

## <a name="remarks"></a>Remarques

La propriété **Source** a généralement comme valeur l'identificateur programmatique ou le nom de classe de l'objet. Utilisez la propriété **Source** pour fournir aux utilisateurs des informations lorsque votre code est incapable de gérer une erreur générée dans un objet d'une autre application.

Par exemple, si vous accédez à Microsoft Excel et qu’il génère une erreur « Division par zéro », Microsoft Excel définit **Error.Number** sur le code Microsoft Excel pour cette erreur et définit la propriété **Source** sur Excel.Application. Notez que, si l'erreur est générée dans un autre objet appelé par Microsoft Excel, ce dernier intercepte l'erreur et affecte néanmoins le code Microsoft Excel à **Error.Number**. En revanche, les autres propriétés de l'objet **Error** (y compris **Source**) conserveront les valeurs définies par l'objet qui a généré l'erreur. La propriété **Source** contient toujours le nom de l'objet qui a initialement généré l'erreur.

Vous pouvez écrire du code qui gèrera l'erreur de façon adaptée, en vous basant sur toute la documentation relative aux erreurs. Si votre gestionnaire d'erreurs échoue, vous pouvez utiliser les informations de l'objet **[Error](error-object-dao.md)** pour décrire l'erreur à vos utilisateurs, à l'aide de la propriété **Source** et des autres propriétés de l'objet **Error** afin que que ceux-ci disposent d'informations sur l'objet à l'origine de l'erreur, d'une description de l'erreur, etc.


> [!NOTE]
> [!REMARQUE] La construction **On Error Resume Next** est parfois préférable à la construction **On Error GoTo** lorsqu'il s'agit d'erreurs générées au cours de l'accès à d'autres objets. Lorsque vous vérifiez la propriété de l'objet **Error** après chaque interaction avec un objet, vous pouvez identifier précisément l'objet auquel votre code accédait au moment de l'erreur. Par conséquent, vous pouvez déterminer avec certitude l'objet qui a placé le code d'erreur dans **Error.Number**, ainsi que l'objet à l'origine de l'erreur (**Error.Source**).

## <a name="example"></a>Exemple

Cet exemple force une erreur, la capture et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet **Error** qui en résulte.

```vb
    Sub DescriptionX() 
     
     Dim dbsTest As Database 
     
     On Error GoTo ErrorHandler 
     
     ' Intentionally trigger an error. 
     Set dbsTest = OpenDatabase("NoDatabase") 
     
     Exit Sub 
     
    ErrorHandler: 
     Dim strError As String 
     Dim errLoop As Error 
     
     ' Enumerate Errors collection and display properties of 
     ' each Error object. 
     For Each errLoop In Errors 
     With errLoop 
     strError = _ 
     "Error #" & .Number & vbCr 
     strError = strError & _ 
     " " & .Description & vbCr 
     strError = strError & _ 
     " (Source: " & .Source & ")" & vbCr 
     strError = strError & _ 
     "Press F1 to see topic " & .HelpContext & vbCr 
     strError = strError & _ 
     " in the file " & .HelpFile & "." 
     End With 
     MsgBox strError 
     Next 
     
     Resume Next 
     
    End Sub
```
