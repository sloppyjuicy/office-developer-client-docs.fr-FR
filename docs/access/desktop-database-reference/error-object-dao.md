---
title: Objet Error-objets d'accès aux données (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3fdfe2091dc2be562f60e5e9cc1935291a74a11d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293475"
---
# <a name="error-object-dao"></a><span data-ttu-id="66365-102">Objet Error (DAO)</span><span class="sxs-lookup"><span data-stu-id="66365-102">Error object (DAO)</span></span>


<span data-ttu-id="66365-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66365-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66365-104">L'objet **Error** contient des détails sur les erreurs d'accès aux données, chacune d'entre elle appartenant à une opération simple impliquant DAO.</span><span class="sxs-lookup"><span data-stu-id="66365-104">**Error** object contains details about data access errors, each of which pertains to a single operation involving DAO.</span></span>

## <a name="remarks"></a><span data-ttu-id="66365-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="66365-105">Remarks</span></span>

<span data-ttu-id="66365-p101">Toute opération impliquant DAO peut générer une ou plusieurs erreurs. Par exemple, un appel à un serveur ODBC peut entraîner une erreur au niveau du serveur de base de données, d'ODBC, et de DAO. Lorsque chacun de ces types d'erreur se produit, un objet **Error** est placé dans la collection **Errors** de l'objet **DBEngine**. Un événement simple peut alors entraîner l'apparition de plusieurs objets **Error** dans la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="66365-p101">Any operation involving DAO can generate one or more errors. For example, a call to an ODBC server might result in an error from the database server, an error from ODBC, and a DAO error. As each such error occurs, an **Error** object is placed in the **Errors** collection of the **DBEngine** object. A single event can therefore result in several **Error** objects appearing in the **Errors** collection.</span></span>

<span data-ttu-id="66365-p102">Lorsqu'une opération DAO suivante génère une erreur, la collection **Errors** est effacée, et un ou plusieurs nouveaux objets **Error** sont placés dans la collection **Errors**. Les opérations DAO qui ne génèrent pas d'erreur n'ont aucun effet sur la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="66365-p102">When a subsequent DAO operation generates an error, the **Errors** collection is cleared, and one or more new **Error** objects are placed in the **Errors** collection. DAO operations that don't generate an error have no effect on the **Errors** collection.</span></span>

<span data-ttu-id="66365-112">Le jeu d'objets **Error** de la collection **Errors** décrit une erreur.</span><span class="sxs-lookup"><span data-stu-id="66365-112">The set of **Error** objects in the **Errors** collection describes one error.</span></span> <span data-ttu-id="66365-113">Le premier objet **Error** est l'erreur de niveau le plus bas (erreur d'origine), la deuxième erreur de niveau supérieur suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="66365-113">The first **Error** object is the lowest level error (the originating error), the second the next higher level error, and so forth.</span></span> <span data-ttu-id="66365-114">Par exemple, si une erreur ODBC se produit lors de la tentative **[](recordset-object-dao.md)** d'ouverture d'un objet Recordset, le premier objet **Error** , **Errors**(0), contient l'erreur ODBC de niveau le plus bas; les erreurs suivantes contiennent les erreurs ODBC renvoyées par les différentes couches d'ODBC.</span><span class="sxs-lookup"><span data-stu-id="66365-114">For example, if an ODBC error occurs while trying to open a **[Recordset](recordset-object-dao.md)** object, the first **Error** object— **Errors**(0)— contains the lowest level ODBC error; subsequent errors contain the ODBC errors returned by the various layers of ODBC.</span></span> <span data-ttu-id="66365-115">Dans ce cas, le gestionnaire de pilote ODBC, voire le pilote lui-même, renvoient des objets **Error** séparés.</span><span class="sxs-lookup"><span data-stu-id="66365-115">In this case, the ODBC driver manager, and possibly the driver itself, return separate **Error** objects.</span></span> <span data-ttu-id="66365-116">Le dernier objet **Error** , **Errors. Count-** 1, contient l'erreur DAO indiquant que l'objet n'a pas pu être ouvert.</span><span class="sxs-lookup"><span data-stu-id="66365-116">The last **Error** object— **Errors.Count-** 1— contains the DAO error indicating that the object couldn't be opened.</span></span>

<span data-ttu-id="66365-p104">L'énumération des erreurs spécifiques dans la collection **Errors** permet à vos programmes de traitement des erreurs de déterminer plus précisément la cause et l'origine d'une erreur, et entreprend la procédure appropriée pour effectuer la récupération. Vous pouvez lire les propriétés de l'objet **Error** afin d'obtenir des détails spécifiques sur chaque erreur, notamment :</span><span class="sxs-lookup"><span data-stu-id="66365-p104">Enumerating the specific errors in the **Errors** collection enables your error-handling routines to more precisely determine the cause and origin of an error, and take appropriate steps to recover. You can read the **Error** object's properties to obtain specific details about each error, including:</span></span>

  - <span data-ttu-id="66365-119">La propriété **[Description](error-description-property-dao.md)**, qui contient le texte de l'alerte d'erreur qui va être affichée à l'écran si l'erreur n'est pas interceptée.</span><span class="sxs-lookup"><span data-stu-id="66365-119">The **[Description](error-description-property-dao.md)** property, which contains the text of the error alert that will be displayed on the screen if the error is not trapped.</span></span>

  - <span data-ttu-id="66365-120">La propriété **[Number](error-number-property-dao.md)**, qui contient la valeur d'entier long de la constante d'erreur.</span><span class="sxs-lookup"><span data-stu-id="66365-120">The **[Number](error-number-property-dao.md)** property, which contains the Long integer value of the error constant.</span></span>

  - <span data-ttu-id="66365-p105">La propriété **[Source](error-source-property-dao.md)**, qui identifie l'objet qui a généré l'erreur. Cela s'avère particulièrement utile lorsque la collection **Errors** contient plusoeurs objets **Error** suite à une demande auprès d'une source de données ODBC.</span><span class="sxs-lookup"><span data-stu-id="66365-p105">The **[Source](error-source-property-dao.md)** property, which identifies the object that raised the error. This is particularly useful when you have several **Error** objects in the **Errors** collection following a request to an ODBC data source.</span></span>

  - <span data-ttu-id="66365-123">Les propriétés **HelpFile** et **HelpContext**, qui indiquent respectivement le fichier d'aide et la rubrique d'aide Microsoft Windows appropriés (le cas échéant) pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="66365-123">The **HelpFile** and **HelpContext** properties, which indicate the appropriate Microsoft Windows Help file and Help topic, respectively, (if any exist) for the error.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="66365-124">[!REMARQUE] Lors de la programmation dans Microsoft Visual Basic pour Applications (VBA), si vous utilisez le mot clé **New** pour créer un objet qui entraîne consécutivement une erreur avant que cet objet soit ajouté à une collection, la collection **Errors** de l'objet **DBEngine** ne contient pas d'entrée pour l'erreur de cet objet, car le nouvel objet est associé à l'objet **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="66365-124">When programming in Microsoft Visual Basic for Applications (VBA), if you use the **New** keyword to create an object that subsequently causes an error before that object has been appended to a collection, the **DBEngine** object's **Errors** collection won't contain an entry for that object's error, because the new object is not associated with the **DBEngine** object.</span></span> <span data-ttu-id="66365-125">Cependant, les informations d'erreur sont disponibles dans l'objet VBA **Err**.</span><span class="sxs-lookup"><span data-stu-id="66365-125">However, the error information is available in the VBA **Err** object.</span></span> <span data-ttu-id="66365-126">Le code de traitement des erreurs VBA doit examiner la collection **Errors** chaque fois que vous anticipez une erreur d'accès aux données.</span><span class="sxs-lookup"><span data-stu-id="66365-126">Your VBA error-handling code should examine the **Errors** collection whenever you anticipate a data access error.</span></span> 
    > 
    > <span data-ttu-id="66365-127">Si vous écrivez un gestionnaire d'erreur centralisé, testez l'objet VBA **Err** pour déterminer si les informations d'erreur dans la collection **Errors** sont valides.</span><span class="sxs-lookup"><span data-stu-id="66365-127">If you are writing a centralized error handler, test the VBA **Err** object to determine if the error information in the **Errors** collection is valid.</span></span> <span data-ttu-id="66365-128">Si la propriété **Number** du dernier élément de la collection **Errors** (DBEngine. Errors. Count-1) et la valeur de l'objet **Err** correspondent, vous pouvez utiliser une série d'instructions **Select Case** pour identifier l'erreur DAO ou erreurs qui se sont produites.</span><span class="sxs-lookup"><span data-stu-id="66365-128">If the **Number** property of the last element of the **Errors** collection (DBEngine.Errors.Count - 1) and the value of the **Err** object match, you can then use a series of **Select Case** statements to identify the particular DAO error or errors that occurred.</span></span> <span data-ttu-id="66365-129">Si elles ne correspondent pas, utilisez la méthode [Refresh](errors-refresh-method-dao.md) dans la collection **Errors**.</span><span class="sxs-lookup"><span data-stu-id="66365-129">If they do not match, use the [Refresh](errors-refresh-method-dao.md) method on the **Errors** collection.</span></span>



## <a name="example"></a><span data-ttu-id="66365-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="66365-130">Example</span></span>

<span data-ttu-id="66365-131">Cet exemple force une erreur, la capture et affiche les propriétés **Description**, **Number**, **Source**, **HelpContext** et **HelpFile** de l'objet **Error** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="66365-131">This example forces an error, traps it, and displays the **Description**, **Number**, **Source**, **HelpContext**, and **HelpFile** properties of the resulting **Error** object.</span></span>

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
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

