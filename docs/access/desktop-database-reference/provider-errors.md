---
title: Erreurs de fournisseur (référence de base de données de bureau Access)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d175cdaa007a354d12304dceff0352a923de2291
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301126"
---
# <a name="provider-errors"></a><span data-ttu-id="2d0ca-102">Erreurs de fournisseur</span><span class="sxs-lookup"><span data-stu-id="2d0ca-102">Provider errors</span></span>


<span data-ttu-id="2d0ca-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d0ca-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="2d0ca-p101">Lorsqu'une erreur de fournisseur survient, une erreur d'exécution -2147467259 est renvoyée. Lorsque vous recevez cette erreur, vérifiez la collection **Errors** de l'objet **Connection**, qui contient une ou plusieurs erreurs décrivant ce qu'il s'est passé.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p101">When a provider error occurs, a run-time error of -2147467259 is returned. When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="2d0ca-106">Collection Errors ADO</span><span class="sxs-lookup"><span data-stu-id="2d0ca-106">The ADO Errors Collection</span></span>

<span data-ttu-id="2d0ca-p102">Parce qu'une opération ADO particulière peut produire plusieurs erreurs de fournisseur, ADO expose une collection des objets d'erreur via l'objet **Connection**. Cette collection ne contient aucun objet si une opération se déroule sans problème, et contient un ou plusieurs objets **Error** si l'opération a échoué et le fournisseur a déclenché une ou plusieurs erreurs. Examinez chaque objet d'erreur individuelle afin de déterminer la cause exacte de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p102">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object. This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors. Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="2d0ca-p103">Lorsque vous avez résolu toutes les erreurs survenues, vous pouvez effacer la collection en invoquant la méthode **Clear**. Il est particulièrement important d'effacer explicitement la collection **Errors** avant d'invoquer la méthode **Resync**, **UpdateBatch** ou **CancelBatch** sur un objet **Recordset**, la méthode **Open** sur un objet **Connection** ou de définir la propriété **Filter** sur un objet **Recordset**. En effaçant la collection explicitement, vous pouvez être sûr qu'aucun objet **Error** de la collection ne subsiste d'une opération antérieure.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p103">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method. It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object. By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="2d0ca-p104">Certaines opérations peuvent générer des avertissements comme des erreurs. Les avertissements sont également représentés par les objets **Error** de la collection **Errors**. Lorsqu'un fournisseur ajoute un avertissement à la collection, aucune erreur d'exécution n'est générée. Vérifiez la propriété **Count** de la collection **Errors** pour déterminer si un avertissement était dû à une opération spécifique. Si cette propriété est supérieure ou égale à 1, un objet **Error** a été ajouté à la collection. Une fois que avez déterminé que la collection **Errors** contient des erreurs ou des avertissements, vous pouvez effectuer une itération de la collection et extraire des informations sur chacun des objets **Error** qu'elle contient. Le court exemple Visual Basic suivant illustre cela :</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p104">Some operations can generate warnings as well as errors. Warnings are also represented by **Error** objects in the **Errors** collection. When a provider adds a warning to the collection, it does not generate a run-time error. Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation. If the count is one or greater, an **Error** object has been added to the collection. Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains. The following short Visual Basic example demonstrates this:</span></span>

```vb 
 
' BeginErrorHandlingVB02 
Private Function DeleteCustomer(ByVal CompanyName As String) As Long 
 On Error GoTo DeleteCustomerError 
 
 rst.Find "CompanyName='" & CompanyName & "'" 
 
DeleteCustomerError: 
 
 Dim objError As ADODB.Error 
 Dim strError As String 
 
 If cnn.Errors.Count > 0 Then 
 For Each objError In cnn.Errors 
 strError = strError & "Error #" & objError.Number & _ 
 " " & objError.Description & vbCrLf & _ 
 "NativeError: " & objError.NativeError & vbCrLf & _ 
 "SQLState: " & objError.SQLState & vbCrLf & _ 
 "Reported by: " & objError.Source & vbCrLf & _ 
 "Help file: " & objError.HelpFile & vbCrLf & _ 
 "Help Context ID: " & objError.HelpContext 
 Next 
 MsgBox strError 
 End If 
End Function 
' EndErrorHandlingVB02 
```

<span data-ttu-id="2d0ca-p105">Le programme de gestion des erreurs comprend une boucle **For Each** qui examine chaque objet de la collection **Errors**. Dans cet exemple, il accumule simplement un message à afficher. Dans un programme de travail, vous pourriez écrire un code permettant d'effectuer une tâche appropriée pour chaque erreur, comme fermer tous les fichiers ouverts et fermer le programme de manière ordonnée.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p105">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection. In this example, it simply accumulates a message for display. In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="2d0ca-123">Objet Error</span><span class="sxs-lookup"><span data-stu-id="2d0ca-123">The Error Object</span></span>

<span data-ttu-id="2d0ca-p106">En examinant un objet **Error**, vous pouvez déterminer le type d'erreur survenue et, plus important encore, l'application ou l'objet à l'origine de l'erreur. L'objet **Error** a les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p106">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error. The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d0ca-126">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="2d0ca-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="2d0ca-127">Description</span><span class="sxs-lookup"><span data-stu-id="2d0ca-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d0ca-128"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="2d0ca-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="2d0ca-129">Une description textuelle de l'erreur survenue.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d0ca-130"><strong>HelpContext, HelpFile</strong></span><span class="sxs-lookup"><span data-stu-id="2d0ca-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="2d0ca-131">Fait référence à la rubrique d'aide et au fichier d'aide qui contient une description de l'erreur survenue.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d0ca-132"><strong>NativeError</strong></span><span class="sxs-lookup"><span data-stu-id="2d0ca-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="2d0ca-133">Le numéro d'erreur spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d0ca-134"><strong>Number</strong></span><span class="sxs-lookup"><span data-stu-id="2d0ca-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="2d0ca-135">Un entier long qui représente le numéro (indiqué dans <strong>ErrorValueEnum</strong>) de l'erreur survenue.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d0ca-136"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="2d0ca-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="2d0ca-137">Indique le nom de l'objet ou de l'application à l'origine d'une erreur.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d0ca-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="2d0ca-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="2d0ca-139">Un code d'erreur à cinq caractères que le fournisseur renvoie au cours du processus d'une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2d0ca-p107">L'objet **Error** ADO est assez similaire à l'objet Visual Basic **Err** standard. Ces propriétés décrivent l'erreur survenue. En plus du numéro de l'erreur, deux autres informations sont fournies. La propriété **NativeError** contient un numéro d'erreur spécifique au fournisseur que vous utilisez. Dans l'exemple précédent, le fournisseur est Microsoft OLE DB Provider for SQL Server. La propriété **NativeError** contient donc des erreurs spécifiques à SQL Server. La propriété **SQLState** contient un code à cinq caractères qui décrit une erreur dans une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p107">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object. Its properties describe the error that occurred. In addition to the number of the error, you also receive two related pieces of information. The **NativeError** property contains an error number specific to the provider you are using. In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server. The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="2d0ca-146">Erreurs liées aux événements</span><span class="sxs-lookup"><span data-stu-id="2d0ca-146">Event-Related Errors</span></span>

<span data-ttu-id="2d0ca-p108">L'objet **Error** est également utilisé lorsqu'une erreur liée aux événements survient. Vous pouvez déterminer si une erreur est survenue dans le processus qui a déclenché un événement ADO en vérifiant l'objet **Error** transféré en tant que paramètre d'événement.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p108">The **Error** object is also used when event-related errors occur. You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="2d0ca-p109">Si l'opération qui provoque un événement se termine correctement, le paramètre *adStatus* du gestionnaire d'événements est défini sur *adStatusOK*. D'autre part, si l'opération qui a déclenché l'événement à échoué, le paramètre *adStatus* est défini sur *adStatusErrorsOccurred*. Dans ce cas, le paramètre *pError* contient un objet **Error** qui décrit l'erreur.</span><span class="sxs-lookup"><span data-stu-id="2d0ca-p109">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*. On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*. In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

