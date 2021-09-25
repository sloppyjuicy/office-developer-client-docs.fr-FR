---
title: ExecuteComplete, événement (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f451d61b228d85abb16f5d5e08e0fdd40b1c2d55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597344"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete, événement (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **ExecuteComplete** est appelé au terme de l'exécution d'une commande.

## <a name="syntax"></a>Syntaxe

ExecuteComplete *RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*RecordsAffected* |Valeur de type **Long** indiquant le nombre d'enregistrements affectés par la commande.|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.|
|*pCommand* |The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.|
|*pRecordset* |Objet [Recordset](recordset-object-ado.md) résultant de la commande exécutée. Cet objet **Recordset** peut être vide. Il ne doit jamais être détruit à partir de ce gestionnaire d'événements. En effet, cela entraîne une violation d'accès puisqu'ADO tente d'accéder à un objet qui n'existe plus.|
|*pConnection* |Objet [Connection](connection-object-ado.md), représentant la connexion utilisée pour l'exécution de l'opération.|

## <a name="remarks"></a>Remarques

Un événement **ExecuteComplete** peut se produire avec les méthodes **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) ou **Recordset.**[NextRecordset](nextrecordset-method-ado.md).

