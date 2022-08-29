---
title: ExecuteComplete event (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 359447f14284e29fd2a82b690c69aa3401bf8a55
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365956"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete event (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **ExecuteComplete** est appelé au terme de l'exécution d'une commande.

## <a name="syntax"></a>Syntaxe

ExecuteComplete *RecordsAffected*, *pError*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*RecordsAffected* |Valeur de type **Long** indiquant le nombre d'enregistrements affectés par la commande.|
|*Perror* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.|
|*pCommand* |The [Command](command-object-ado.md) object that was executed. Contains a **Command** object even when calling **Connection.Execute** or **Recordset.Open** without explicitly creating a **Command**, in which cases the **Command** object is created internally by ADO.|
|*pRecordset* |Objet [Recordset](recordset-object-ado.md) résultant de la commande exécutée. Cet objet **Recordset** peut être vide. Il ne doit jamais être détruit à partir de ce gestionnaire d'événements. En effet, cela entraîne une violation d'accès puisqu'ADO tente d'accéder à un objet qui n'existe plus.|
|*pConnection* |Objet [Connection](connection-object-ado.md), représentant la connexion utilisée pour l'exécution de l'opération.|

## <a name="remarks"></a>Remarques

Un événement **ExecuteComplete** peut se produire avec les méthodes **Connection.**[Execute](/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) ou **Recordset.**[NextRecordset](nextrecordset-method-ado.md).

