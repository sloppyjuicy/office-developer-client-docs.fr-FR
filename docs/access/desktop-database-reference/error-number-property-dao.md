---
title: Propriété Error.Number (DAO)
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
ms.openlocfilehash: 95d814bb613b848f65b61cd342d2918fbbd2fea2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928340"
---
# <a name="errornumber-property-dao"></a><span data-ttu-id="dd96a-102">Propriété Error.Number (DAO)</span><span class="sxs-lookup"><span data-stu-id="dd96a-102">Error.Number property (DAO)</span></span>


<span data-ttu-id="dd96a-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd96a-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="dd96a-104">Renvoie une valeur numérique spécifiant une erreur.</span><span class="sxs-lookup"><span data-stu-id="dd96a-104">Returns a numeric value specifying an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd96a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd96a-105">Syntax</span></span>

<span data-ttu-id="dd96a-106">*expression* . Nombre</span><span class="sxs-lookup"><span data-stu-id="dd96a-106">*expression* .Number</span></span>

<span data-ttu-id="dd96a-107">*expression* Variable qui représente un objet **Error** .</span><span class="sxs-lookup"><span data-stu-id="dd96a-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd96a-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd96a-108">Remarks</span></span>

<span data-ttu-id="dd96a-p101">La propriété **Number** permet de déterminer l'erreur survenue. La valeur de la propriété correspond à un numéro d'interruption unique qui correspond à une condition d'erreur.</span><span class="sxs-lookup"><span data-stu-id="dd96a-p101">Use the **Number** property to determine the error that occurred. The value of the property corresponds to a unique trap number that corresponds to an error condition.</span></span>

## <a name="example"></a><span data-ttu-id="dd96a-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="dd96a-111">Example</span></span>

<span data-ttu-id="dd96a-112">Cet exemple force une erreur, la capture et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet **Error** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="dd96a-112">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

