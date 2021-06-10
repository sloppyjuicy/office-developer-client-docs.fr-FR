---
title: Error.Number, propriété (DAO)
TOCTitle: Number Property
ms:assetid: 2fb94dca-f990-04f8-bbd2-9919d28de75a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192259(v=office.15)
ms:contentKeyID: 48544013
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053363
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 257c403951eff5bbb2f37de8b38a1c63a3445285
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293496"
---
# <a name="errornumber-property-dao"></a><span data-ttu-id="b987b-102">Error.Number, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="b987b-102">Error.Number property (DAO)</span></span>


<span data-ttu-id="b987b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b987b-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="b987b-104">Renvoie une valeur numérique spécifiant une erreur.</span><span class="sxs-lookup"><span data-stu-id="b987b-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="b987b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b987b-105">Syntax</span></span>

<span data-ttu-id="b987b-106">*.* Number</span><span class="sxs-lookup"><span data-stu-id="b987b-106">*expression* .Number</span></span>

<span data-ttu-id="b987b-107">*expression* Variable qui représente un objet **Error.**</span><span class="sxs-lookup"><span data-stu-id="b987b-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b987b-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="b987b-108">Remarks</span></span>

<span data-ttu-id="b987b-p101">La propriété **Number** permet de déterminer l'erreur survenue. La valeur de la propriété correspond à un numéro d'interruption unique qui correspond à une condition d'erreur.</span><span class="sxs-lookup"><span data-stu-id="b987b-p101">Use the **Number** property to determine the error that occurred. The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="b987b-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="b987b-111">Example</span></span>

<span data-ttu-id="b987b-112">Cet exemple force une erreur, la capture et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet **Error** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="b987b-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

