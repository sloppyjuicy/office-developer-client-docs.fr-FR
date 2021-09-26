---
title: Paramètres d’événement (référence de base de données de bureau Access)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 55b5a3cf20e13bc46568c20a375caf442b8c836b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597414"
---
# <a name="event-parameters"></a>Paramètres d’événement

**S’applique à** : Access 2013, Office 2013

Chaque gestionnaire d'événements comporte un paramètre d'état qui le contrôle. Dans le cas des événements Complete, ce paramètre est également utilisé pour indiquer la réussite ou l'échec de l'opération qui a généré l'événement. La plupart des événements Complete peuvent également comporter un paramètre d'erreur qui fournit des informations concernant une erreur qui a pu se produire, ainsi que des paramètres d'objets qui font référence à des objets ADO utilisés pour effectuer l'opération. Par exemple, l'événement [ExecuteComplete](executecomplete-event-ado.md) comporte des paramètres pour les objets **Command**, **Recordset** et **Connection** associés à l'événement. Dans l'exemple Microsoft Visual Basic suivant, les objets pCommand, pRecordset et pConnection représentent les objets **Command**, **Recordset** et **Connection** utilisés par la méthode **Execute**.

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

À l'exception de l'objet **Error**, les mêmes paramètres sont transmis aux événements Will. Cela vous permet d'examiner chacun des objets à utiliser dans l'opération en attente et de déterminer si l'opération doit être menée à son terme.

Certains gestionnaires d'événements comportent un paramètre *Reason* qui fournit des informations supplémentaires sur la raison du déclenchement d'un événement. Par exemple, les événements **WillMove** et **MoveComplete** peuvent se déclencher à la suite de l'appel d'une méthode de navigation (**MoveNext**, **MovePrevious**, etc.) ou à la suite d'une actualisation.

## <a name="status-parameter"></a>Paramètre Status

Lorsque la routine de gestionnaire d'événements est appelée, le paramètre *Status* est défini avec l'une des valeurs suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>Transmise aux événements Will et Complete. Cette valeur signifie que l'opération qui a déclenché l'événement a réussi.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Transmise uniquement aux événements Complete. Cette valeur signifie que l'opération qui a déclenché l'événement a échoué ou qu'un événement Will a annulé l'opération. Reportez-vous au paramètre <em>Error</em> pour plus de détails.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Transmise uniquement aux événements Will. Cette valeur signifie que l'opération n'a pas pu être annulée par l'événement Will. Elle doit donc être effectuée.</p></td>
</tr>
</tbody>
</table>


Si vous déterminez, dans l'événement Will, que l'opération doit continuer, ne modifiez pas le paramètre *Status*. Toutefois, tant que le paramètre d'état entrant n'a pas la valeur **adStatusCantDeny**, vous pouvez annuler l'opération en attente en appliquant la valeur **adStatusCancel** dans le paramètre *Status*. Ainsi, le paramètre *Status* de l'événement Complete associé à l'opération a la valeur **adStatusErrorsOccurred**. L'objet **Error** transmis à l'événement Complete contiendra la valeur **adErrOperationCancelled**.

Si vous ne voulez plus traiter un événement, affectez au paramètre *Status* la valeur **adStatusUnwantedEvent** et l'application ne recevra plus de notifications de cet événement. N'oubliez pas, toutefois, que certains événements peuvent être déclenchés pour plusieurs raisons. Dans ce cas, vous devez spécifier **adStatusUnwantedEvent** pour chaque raison possible. Par exemple, pour arrêter de recevoir des notifications d'événements **RecordChange** en attente, vous devez définir le paramètre *Status* avec la valeur **adStatusUnwantedEvent** pour **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** et **adRsnFirstChange** au fur et à mesure qu'ils se déclenchent.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>Demande que ce gestionnaire d'événements ne reçoive plus de notifications.</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>Demande l'annulation de l'opération sur le point d'être exécutée.</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>Paramètre Error

Le paramètre *Error* est une référence à un objet [Error](error-object-ado.md) ADO . Lorsque le paramètre *Status* est défini avec la valeur **adStatusErrorsOccurred**, l’objet **Error** contient le détail des raisons de l’échec de l’opération. Si l’événement Will associé à un événement Complete a annulé l’opération en affectant au paramètre *Status* la valeur **adStatusCancel**, l’objet Error est toujours défini avec la valeur **adErrOperationCancelled**.

## <a name="object-parameter"></a>Paramètre Object

Chaque événement reçoit un ou plusieurs objets représentant les objets impliqués dans l'opération. Par exemple, l'événement **ExecuteComplete** reçoit un objet **Command**, un objet **Recordset** et un objet **Connection**.

## <a name="reason-parameter"></a>Paramètre Reason

Le paramètre *Reason*, *adReason*, fournit des informations complémentaires sur la raison de l'événement. Les événements comportant un paramètre *adReason* peuvent être appelés plusieurs fois pour une raison différente, même pour la même opération. Par exemple, le gestionnaire d'événements **WillChangeRecord** est appelé pour les opérations sur le point d'effectuer ou d'annuler l'insertion, la suppression ou la modification d'un enregistrement. Si vous voulez traiter un événement seulement lorsqu'il se déclenche pour une raison particulière, utilisez le paramètre *adReason* pour filtrer les occurrences qui ne vous intéressent pas. Par exemple, si vous voulez traiter des événements de modification d'enregistrements lorsqu'ils se déclenchent à la suite de l'ajout d'un enregistrement, vous pouvez programmer ce qui suit :

```vb 
 
' BeginEventExampleVB01 
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset) 
 If adReason = adRsnAddNew Then 
 ' Process event 
 '... 
 Else 
 ' Cancel event notification for all 
 ' other possible adReason values. 
 adStatus = adStatusUnwantedEvent 
 End If 
End Sub 
' EndEventExampleVB01 
```

Dans ce cas, la notification peut éventuellement se déclencher pour chacune des autres raisons. Cependant, elle ne se produira qu'une fois pour chaque raison. Après avoir reçu une notification pour chaque raison, vous ne recevrez une notification que lors de l'ajout d'un nouvel enregistrement.

En revanche, vous ne devez définir le paramètre *adStatus* avec la valeur **adStatusUnwantedEvent** qu'une seule fois pour demander qu'un gestionnaire d'événements sans paramètre **adReason** ne reçoive plus de notifications d'événements.

