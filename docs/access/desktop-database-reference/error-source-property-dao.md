---
title: Error.Source Property (DAO)
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
ms.openlocfilehash: b9aafe1b16b3d989a81ff21f97bd4b6d10f79de3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471353"
---
# <a name="errorsource-property-dao"></a><span data-ttu-id="ca793-102">Error.Source Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="ca793-102">Error.Source Property (DAO)</span></span>


<span data-ttu-id="ca793-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca793-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="ca793-104">Renvoie le nom de l'objet ou de l'application à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="ca793-104">Returns the name of the object or application that originally generated the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca793-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca793-105">Syntax</span></span>

<span data-ttu-id="ca793-106">*expression* . Source</span><span class="sxs-lookup"><span data-stu-id="ca793-106">*expression* .Source</span></span>

<span data-ttu-id="ca793-107">*expression* Variable qui représente un objet **Error** .</span><span class="sxs-lookup"><span data-stu-id="ca793-107">*expression* A variable that represents an **Error** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca793-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca793-108">Remarks</span></span>

<span data-ttu-id="ca793-p101">La propriété **Source** a généralement comme valeur l'identificateur programmatique ou le nom de classe de l'objet. Utilisez la propriété **Source** pour fournir aux utilisateurs des informations lorsque votre code est incapable de gérer une erreur générée dans un objet d'une autre application.</span><span class="sxs-lookup"><span data-stu-id="ca793-p101">The **Source** property value is usually the object's class name or programmatic ID. Use the **Source** property to provide your users with information when your code is unable to handle an error generated in an object in another application.</span></span>

<span data-ttu-id="ca793-111">Par exemple, si vous accédez à Microsoft Excel et qu’il génère une erreur « Division par zéro », Microsoft Excel affecte à **Error.Number** le code Microsoft Excel de cette erreur et définit la propriété **Source** Excel.Application à la propriété.</span><span class="sxs-lookup"><span data-stu-id="ca793-111">For example, if you access Microsoft Excel and it generates a "Division by zero" error, Microsoft Excel sets **Error.Number** to the Microsoft Excel code for that error and sets the **Source** property to Excel.Application.</span></span> <span data-ttu-id="ca793-112">Notez que, si l'erreur est générée dans un autre objet appelé par Microsoft Excel, ce dernier intercepte l'erreur et affecte néanmoins le code Microsoft Excel à **Error.Number**.</span><span class="sxs-lookup"><span data-stu-id="ca793-112">Note that if the error is generated in another object called by Microsoft Excel, Microsoft Excel intercepts the error and still sets **Error.Number** to the Microsoft Excel code.</span></span> <span data-ttu-id="ca793-113">En revanche, les autres propriétés de l'objet **Error** (y compris **Source**) conserveront les valeurs définies par l'objet qui a généré l'erreur.</span><span class="sxs-lookup"><span data-stu-id="ca793-113">However, the other **Error** object properties (including **Source**) will retain the values as set by the object that generated the error.</span></span> <span data-ttu-id="ca793-114">La propriété **Source** contient toujours le nom de l'objet qui a initialement généré l'erreur.</span><span class="sxs-lookup"><span data-stu-id="ca793-114">The **Source** property always contains the name of the object that originally generated the error.</span></span>

<span data-ttu-id="ca793-p103">Vous pouvez écrire du code qui gèrera l'erreur de façon adaptée, en vous basant sur toute la documentation relative aux erreurs. Si votre gestionnaire d'erreurs échoue, vous pouvez utiliser les informations de l'objet **[Error](error-object-dao.md)** pour décrire l'erreur à vos utilisateurs, à l'aide de la propriété **Source** et des autres propriétés de l'objet **Error** afin que que ceux-ci disposent d'informations sur l'objet à l'origine de l'erreur, d'une description de l'erreur, etc.</span><span class="sxs-lookup"><span data-stu-id="ca793-p103">Based on all of the error documentation, you can write code that will handle the error appropriately. If your error handler fails, you can use the **[Error](error-object-dao.md)** object information to describe the error to your user, using the **Source** property and the other **Error** properties to give the user information about which object originally caused the error, the description of the error, and so forth.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ca793-p104">La construction <STRONG>On Error Resume Next</STRONG> est parfois préférable à la construction <STRONG>On Error GoTo</STRONG> lorsqu'il s'agit d'erreurs générées au cours de l'accès à d'autres objets. Lorsque vous vérifiez la propriété de l'objet <STRONG>Error</STRONG> après chaque interaction avec un objet, vous pouvez identifier précisément l'objet auquel votre code accédait au moment de l'erreur. Par conséquent, vous pouvez déterminer avec certitude l'objet qui a placé le code d'erreur dans <STRONG>Error.Number</STRONG>, ainsi que l'objet à l'origine de l'erreur (<STRONG>Error.Source</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="ca793-p104">The <STRONG>On Error Resume Next</STRONG> construct may be preferable to <STRONG>On Error GoTo</STRONG> when dealing with errors generated during access to other objects. Checking the <STRONG>Error</STRONG> object property after each interaction with an object removes ambiguity about which object your code was accessing when the error occurred. Thus, you can be sure which object placed the error code in <STRONG>Error.Number</STRONG>, as well as which object originally generated the error (<STRONG>Error.Source</STRONG>).</span></span></P>



## <a name="example"></a><span data-ttu-id="ca793-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="ca793-120">Example</span></span>

<span data-ttu-id="ca793-121">Cet exemple force une erreur, la capture et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet **Error** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="ca793-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
