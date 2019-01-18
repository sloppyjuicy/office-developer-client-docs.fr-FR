---
title: Propriété Error.Description (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 1d7e949771e764c22e93ef56059930ccf39584ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714562"
---
# <a name="errordescription-property-dao"></a><span data-ttu-id="7d334-102">Propriété Error.Description (DAO)</span><span class="sxs-lookup"><span data-stu-id="7d334-102">Error.Description property (DAO)</span></span>


<span data-ttu-id="7d334-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d334-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="7d334-p101">Renvoie une chaîne descriptive associée à une erreur. Il s'agit de la propriété par défaut de l'objet **Error**.</span><span class="sxs-lookup"><span data-stu-id="7d334-p101">Returns a descriptive string associated with an error. This is the default property for the **Error** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d334-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d334-106">Syntax</span></span>

<span data-ttu-id="7d334-107">*expression* . Description</span><span class="sxs-lookup"><span data-stu-id="7d334-107">*expression* .Description</span></span>

<span data-ttu-id="7d334-108">*expression* Variable qui représente un objet **Error** .</span><span class="sxs-lookup"><span data-stu-id="7d334-108">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d334-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d334-109">Remarks</span></span>

<span data-ttu-id="7d334-p102">La propriété **Description** comprend une brève description de l'erreur. Elle permet de signaler à l'utilisateur la présence d'une erreur que vous ne pouvez ou ne souhaitez pas gérer.</span><span class="sxs-lookup"><span data-stu-id="7d334-p102">The **Description** property comprises a short description of the error. Use this property to alert the user about an error that you cannot or do not want to handle.</span></span>

## <a name="example"></a><span data-ttu-id="7d334-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="7d334-112">Example</span></span>

<span data-ttu-id="7d334-113">L'exemple ci-dessous force une erreur, l'intercepte et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="7d334-113">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting Error object.</span></span>

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

