---
title: Paramètres de l’événement (référence de base de données du bureau Access)
TOCTitle: Event Parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 023109586d13dc25846c8c145746aaf97fc22c15
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888369"
---
# <a name="event-parameters"></a><span data-ttu-id="47848-102">Paramètres d’événement</span><span class="sxs-lookup"><span data-stu-id="47848-102">Event Parameters</span></span>


<span data-ttu-id="47848-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47848-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="47848-p101">Chaque gestionnaire d'événements comporte un paramètre d'état qui le contrôle. Dans le cas des événements Complete, ce paramètre est également utilisé pour indiquer la réussite ou l'échec de l'opération qui a généré l'événement. La plupart des événements Complete peuvent également comporter un paramètre d'erreur qui fournit des informations concernant une erreur qui a pu se produire, ainsi que des paramètres d'objets qui font référence à des objets ADO utilisés pour effectuer l'opération. Par exemple, l'événement [ExecuteComplete](executecomplete-event-ado.md) comporte des paramètres pour les objets **Command**, **Recordset** et **Connection** associés à l'événement. Dans l'exemple Microsoft Visual Basic suivant, les objets pCommand, pRecordset et pConnection représentent les objets **Command**, **Recordset** et **Connection** utilisés par la méthode **Execute**.</span><span class="sxs-lookup"><span data-stu-id="47848-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="47848-p102">À l'exception de l'objet **Error**, les mêmes paramètres sont transmis aux événements Will. Cela vous permet d'examiner chacun des objets à utiliser dans l'opération en attente et de déterminer si l'opération doit être menée à son terme.</span><span class="sxs-lookup"><span data-stu-id="47848-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="47848-p103">Certains gestionnaires d'événements comportent un paramètre *Reason* qui fournit des informations supplémentaires sur la raison du déclenchement d'un événement. Par exemple, les événements **WillMove** et **MoveComplete** peuvent se déclencher à la suite de l'appel d'une méthode de navigation (**MoveNext**, **MovePrevious**, etc.) ou à la suite d'une actualisation.</span><span class="sxs-lookup"><span data-stu-id="47848-p103">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred. For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="47848-113">Paramètre Status</span><span class="sxs-lookup"><span data-stu-id="47848-113">Status Parameter</span></span>

<span data-ttu-id="47848-114">Lorsque la routine de gestionnaire d'événements est appelée, le paramètre *Status* est défini avec l'une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="47848-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47848-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47848-115">Value</span></span></p></th>
<th><p><span data-ttu-id="47848-116">Description</span><span class="sxs-lookup"><span data-stu-id="47848-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47848-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="47848-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="47848-p104">Transmise aux événements Will et Complete. Cette valeur signifie que l'opération qui a déclenché l'événement a réussi.</span><span class="sxs-lookup"><span data-stu-id="47848-p104">Passed to both Will and Complete events. This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47848-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="47848-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="47848-p105">Transmise uniquement aux événements Complete. Cette valeur signifie que l'opération qui a déclenché l'événement a échoué ou qu'un événement Will a annulé l'opération. Reportez-vous au paramètre <em>Error</em> pour plus de détails.</span><span class="sxs-lookup"><span data-stu-id="47848-p105">Passed to Complete events only. This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation. Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47848-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="47848-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="47848-p106">Transmise uniquement aux événements Will. Cette valeur signifie que l'opération n'a pas pu être annulée par l'événement Will. Elle doit donc être effectuée.</span><span class="sxs-lookup"><span data-stu-id="47848-p106">Passed to Will events only. This value means that the operation cannot be canceled by the Will event. It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47848-p107">Si vous déterminez, dans l'événement Will, que l'opération doit continuer, ne modifiez pas le paramètre *Status*. Toutefois, tant que le paramètre d'état entrant n'a pas la valeur **adStatusCantDeny**, vous pouvez annuler l'opération en attente en appliquant la valeur **adStatusCancel** dans le paramètre *Status*. Ainsi, le paramètre *Status* de l'événement Complete associé à l'opération a la valeur **adStatusErrorsOccurred**. L'objet **Error** transmis à l'événement Complete contiendra la valeur **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="47848-p107">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged. As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**. When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**. The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="47848-p108">Si vous ne voulez plus traiter un événement, affectez au paramètre *Status* la valeur **adStatusUnwantedEvent** et l'application ne recevra plus de notifications de cet événement. N'oubliez pas, toutefois, que certains événements peuvent être déclenchés pour plusieurs raisons. Dans ce cas, vous devez spécifier **adStatusUnwantedEvent** pour chaque raison possible. Par exemple, pour arrêter de recevoir des notifications d'événements **RecordChange** en attente, vous devez définir le paramètre *Status* avec la valeur **adStatusUnwantedEvent** pour **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** et **adRsnFirstChange** au fur et à mesure qu'ils se déclenchent.</span><span class="sxs-lookup"><span data-stu-id="47848-p108">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event. Remember, however, that some events can be raised for more than one reason. In that case, you must specify **adStatusUnwantedEvent** for each possible reason. For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47848-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="47848-136">Value</span></span></p></th>
<th><p><span data-ttu-id="47848-137">Description</span><span class="sxs-lookup"><span data-stu-id="47848-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47848-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="47848-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="47848-139">Demande que ce gestionnaire d'événements ne reçoive plus de notifications.</span><span class="sxs-lookup"><span data-stu-id="47848-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47848-140"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="47848-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="47848-141">Demande l'annulation de l'opération sur le point d'être exécutée.</span><span class="sxs-lookup"><span data-stu-id="47848-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="47848-142">Paramètre Error</span><span class="sxs-lookup"><span data-stu-id="47848-142">Error Parameter</span></span>

<span data-ttu-id="47848-143">Le paramètre *Error* est une référence à un objet ADO [erreur](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="47848-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="47848-144">Lorsque le paramètre *Status* est défini avec la **valeur adStatusErrorsOccurred**, l’objet **Error** contient plus d’informations sur l’échec de l’opération.</span><span class="sxs-lookup"><span data-stu-id="47848-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="47848-145">Si l’événement Will associé à un événement Complete a annulé l’opération en définissant le paramètre *Status* à **adStatusCancel**, l’objet error est toujours défini avec la **valeur adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="47848-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="47848-146">Paramètre Object</span><span class="sxs-lookup"><span data-stu-id="47848-146">Object Parameter</span></span>

<span data-ttu-id="47848-p110">Chaque événement reçoit un ou plusieurs objets représentant les objets impliqués dans l'opération. Par exemple, l'événement **ExecuteComplete** reçoit un objet **Command**, un objet **Recordset** et un objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="47848-p110">Each event receives one or more objects representing the objects that are involved in the operation. For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="47848-149">Paramètre Reason</span><span class="sxs-lookup"><span data-stu-id="47848-149">Reason Parameter</span></span>

<span data-ttu-id="47848-p111">Le paramètre *Reason*, *adReason*, fournit des informations complémentaires sur la raison de l'événement. Les événements comportant un paramètre *adReason* peuvent être appelés plusieurs fois pour une raison différente, même pour la même opération. Par exemple, le gestionnaire d'événements **WillChangeRecord** est appelé pour les opérations sur le point d'effectuer ou d'annuler l'insertion, la suppression ou la modification d'un enregistrement. Si vous voulez traiter un événement seulement lorsqu'il se déclenche pour une raison particulière, utilisez le paramètre *adReason* pour filtrer les occurrences qui ne vous intéressent pas. Par exemple, si vous voulez traiter des événements de modification d'enregistrements lorsqu'ils se déclenchent à la suite de l'ajout d'un enregistrement, vous pouvez programmer ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="47848-p111">The *Reason* parameter, *adReason*, provides additional information about why the event occurred. Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason. For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record. If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in. For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

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

<span data-ttu-id="47848-p112">Dans ce cas, la notification peut éventuellement se déclencher pour chacune des autres raisons. Cependant, elle ne se produira qu'une fois pour chaque raison. Après avoir reçu une notification pour chaque raison, vous ne recevrez une notification que lors de l'ajout d'un nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="47848-p112">In this case, notification can potentially occur for each of the other reasons. However, it will occur only once for each reason. After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="47848-158">En revanche, vous devez définir le paramètre *adStatus* avec la **valeur adStatusUnwantedEvent** qu’une seule fois pour demander qu’un gestionnaire d’événements sans **paramètre adReason recevoir des notifications d’événement** .</span><span class="sxs-lookup"><span data-stu-id="47848-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

