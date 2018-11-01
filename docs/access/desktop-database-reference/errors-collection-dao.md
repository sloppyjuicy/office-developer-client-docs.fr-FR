---
title: Errors Collection (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: debc3554fb63ab379bbc94bc8d44e2239eb32dd4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885751"
---
# <a name="errors-collection-dao"></a><span data-ttu-id="d6672-102">Errors Collection (DAO)</span><span class="sxs-lookup"><span data-stu-id="d6672-102">Errors Collection (DAO)</span></span>


<span data-ttu-id="d6672-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6672-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6672-104">Une collection **Errors** contient tous les objets **Error** stockés, chacun se rapportant à une opération unique impliquant DAO.</span><span class="sxs-lookup"><span data-stu-id="d6672-104">An **Errors** collection contains all stored **Error** objects, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6672-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6672-105">Remarks</span></span>

<span data-ttu-id="d6672-p101">Toute opération impliquant des objets DAO peut générer une ou plusieurs erreurs. À mesure que les erreurs surviennent, un ou plusieurs objets **Error** sont stockés dans la collection **Errors** de l'objet **DBEngine**. Lorsqu'une autre opération DAO génère une erreur, la collection **Errors** est effacée et le nouveau jeu d'objets **Error** est stocké dans la collection **Errors**. L'objet au numéro le plus élevé dans la collection \*\*Errors \*\*(DBEngine.Errors.Count - 1) correspond à l'erreur signalée par l'objet **Err** de Microsoft Visual Basic for Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="d6672-p101">Any operation involving DAO objects can generate one or more errors. As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **DBEngine** object. When another DAO operation generates an error, the **Errors** collection is cleared, and the new set of **Error** objects is placed in the **Errors** collection. The highest-numbered object in the **Errors** collection (DBEngine.Errors.Count - 1) corresponds to the error reported by the Microsoft Visual Basic for Applications (VBA) **Err** object.</span></span>

<span data-ttu-id="d6672-110">Les opérations DAO ne générant aucune erreur n'ont pas d'effets sur la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="d6672-110">DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="d6672-111">Les éléments de la collection **Errors** ne sont pas ajoutés comme ils le sont d'ordinaire avec les autres collections. Par conséquent, la collection **Errors** ne prend pas en charge les méthodes **Append** et **Delete**.</span><span class="sxs-lookup"><span data-stu-id="d6672-111">Elements of the **Errors** collection aren't appended as they typically are with other collections, so the **Errors** collection doesn't support the **Append** and **Delete** methods.</span></span>

<span data-ttu-id="d6672-p102">Le jeu d'objets **Error** de la collection **Errors** décrit une erreur. Le premier objet **Error** correspond à l'erreur de niveau le plus bas, le second au niveau immédiatement supérieur, etc. Par exemple, si une erreur ODBC survient lors de l'ouverture d'un objet **[Recordset](recordset-object-dao.md)**, le premier objet Error contient l'erreur ODBC de niveau le plus faible ; les erreurs suivantes contiennent les erreurs ODBC renvoyées par les différentes couches d'ODBC. Dans ce cas, le gestionnaire de pilote ODBC, voire le pilote lui-même, renvoient des objets **Error** séparés. Le dernier objet **Error** contient l'erreur DAO indiquant que l'objet n'a pas pu être ouvert.</span><span class="sxs-lookup"><span data-stu-id="d6672-p102">The set of **Error** objects in the **Errors** collection describes one error. The first **Error** object is the lowest level error, the second the next higher level, and so forth. For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first error object contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC. In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects. The last **Error** object contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="d6672-117">L'énumération des différentes erreurs dans la collection **Errors** permet à vos routines de gestion des erreurs de déterminer de manière plus précise la cause et l'origine d'une erreur et de prendre les dispositions appropriées pour la résoudre.</span><span class="sxs-lookup"><span data-stu-id="d6672-117">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover.</span></span>


> [!NOTE]
> <span data-ttu-id="d6672-p103">[!REMARQUE] Si vous utilisez le mot clé **New** pour créer un objet à l'origine d'une erreur avant ou au moment d'être placé dans la collection **Errors**, cette dernière ne contient pas les informations d'erreur de cet objet, car le nouvel objet n'est pas associé à l'objet **DBEngine**. Toutefois, les informations d'erreur sont disponibles dans l'objet VBA **Err**.</span><span class="sxs-lookup"><span data-stu-id="d6672-p103">If you use the **New** keyword to create an object that causes an error either before or while being placed into the **Errors** collection, the collection doesn't contain error information about that object, because the new object is not associated with the **DBEngine** object. However, the error information is available in the VBA **Err** object.</span></span>

## <a name="example"></a><span data-ttu-id="d6672-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="d6672-120">Example</span></span>

<span data-ttu-id="d6672-121">Cet exemple force une erreur, la capture et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet **Error** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="d6672-121">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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

