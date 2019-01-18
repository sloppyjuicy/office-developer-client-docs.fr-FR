---
title: Erreurs du fournisseur (référence de base de données du bureau Access)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d175cdaa007a354d12304dceff0352a923de2291
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717642"
---
# <a name="provider-errors"></a>Erreurs de fournisseur


**S’applique à**: Access 2013, Office 2013 

Lorsqu'une erreur de fournisseur survient, une erreur d'exécution -2147467259 est renvoyée. Lorsque vous recevez cette erreur, vérifiez la collection **Errors** de l'objet **Connection**, qui contient une ou plusieurs erreurs décrivant ce qu'il s'est passé.

## <a name="the-ado-errors-collection"></a>Collection Errors ADO

Parce qu'une opération ADO particulière peut produire plusieurs erreurs de fournisseur, ADO expose une collection des objets d'erreur via l'objet **Connection**. Cette collection ne contient aucun objet si une opération se déroule sans problème, et contient un ou plusieurs objets **Error** si l'opération a échoué et le fournisseur a déclenché une ou plusieurs erreurs. Examinez chaque objet d'erreur individuelle afin de déterminer la cause exacte de l'erreur.

Lorsque vous avez résolu toutes les erreurs survenues, vous pouvez effacer la collection en invoquant la méthode **Clear**. Il est particulièrement important d'effacer explicitement la collection **Errors** avant d'invoquer la méthode **Resync**, **UpdateBatch** ou **CancelBatch** sur un objet **Recordset**, la méthode **Open** sur un objet **Connection** ou de définir la propriété **Filter** sur un objet **Recordset**. En effaçant la collection explicitement, vous pouvez être sûr qu'aucun objet **Error** de la collection ne subsiste d'une opération antérieure.

Certaines opérations peuvent générer des avertissements comme des erreurs. Les avertissements sont également représentés par les objets **Error** de la collection **Errors**. Lorsqu'un fournisseur ajoute un avertissement à la collection, aucune erreur d'exécution n'est générée. Vérifiez la propriété **Count** de la collection **Errors** pour déterminer si un avertissement était dû à une opération spécifique. Si cette propriété est supérieure ou égale à 1, un objet **Error** a été ajouté à la collection. Une fois que avez déterminé que la collection **Errors** contient des erreurs ou des avertissements, vous pouvez effectuer une itération de la collection et extraire des informations sur chacun des objets **Error** qu'elle contient. Le court exemple Visual Basic suivant illustre cela :

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

Le programme de gestion des erreurs comprend une boucle **For Each** qui examine chaque objet de la collection **Errors**. Dans cet exemple, il accumule simplement un message à afficher. Dans un programme de travail, vous pourriez écrire un code permettant d'effectuer une tâche appropriée pour chaque erreur, comme fermer tous les fichiers ouverts et fermer le programme de manière ordonnée.

## <a name="the-error-object"></a>Objet Error

En examinant un objet **Error**, vous pouvez déterminer le type d'erreur survenue et, plus important encore, l'application ou l'objet à l'origine de l'erreur. L'objet **Error** a les propriétés suivantes :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de la propriété</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Description</strong></p></td>
<td><p>Une description textuelle de l'erreur survenue.</p></td>
</tr>
<tr class="even">
<td><p><strong>HelpContext, HelpFile</strong></p></td>
<td><p>Fait référence à la rubrique d'aide et au fichier d'aide qui contient une description de l'erreur survenue.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>Le numéro d'erreur spécifique au fournisseur.</p></td>
</tr>
<tr class="even">
<td><p><strong>Number</strong></p></td>
<td><p>Un entier long qui représente le numéro (indiqué dans <strong>ErrorValueEnum</strong>) de l'erreur survenue.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Indique le nom de l'objet ou de l'application à l'origine d'une erreur.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>Un code d'erreur à cinq caractères que le fournisseur renvoie au cours du processus d'une instruction SQL.</p></td>
</tr>
</tbody>
</table>


L'objet **Error** ADO est assez similaire à l'objet Visual Basic **Err** standard. Ces propriétés décrivent l'erreur survenue. En plus du numéro de l'erreur, deux autres informations sont fournies. La propriété **NativeError** contient un numéro d'erreur spécifique au fournisseur que vous utilisez. Dans l'exemple précédent, le fournisseur est Microsoft OLE DB Provider for SQL Server. La propriété **NativeError** contient donc des erreurs spécifiques à SQL Server. La propriété **SQLState** contient un code à cinq caractères qui décrit une erreur dans une instruction SQL.

## <a name="event-related-errors"></a>Erreurs liées aux événements

L'objet **Error** est également utilisé lorsqu'une erreur liée aux événements survient. Vous pouvez déterminer si une erreur est survenue dans le processus qui a déclenché un événement ADO en vérifiant l'objet **Error** transféré en tant que paramètre d'événement.

Si l'opération qui provoque un événement se termine correctement, le paramètre *adStatus* du gestionnaire d'événements est défini sur *adStatusOK*. D'autre part, si l'opération qui a déclenché l'événement à échoué, le paramètre *adStatus* est défini sur *adStatusErrorsOccurred*. Dans ce cas, le paramètre *pError* contient un objet **Error** qui décrit l'erreur.

