---
title: ExecuteComplete, événement (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 58683a8721ede0e7535b159f095b44bc6db6c1b7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926730"
---
# <a name="executecomplete-event-ado"></a>ExecuteComplete, événement (ADO)


**S’applique à**: Access 2013, Office 2013



L'événement **ExecuteComplete** est appelé au terme de l'exécution d'une commande.

## <a name="syntax"></a>Syntaxe

ExecuteComplete*RecordsAffected* *pError*, *adStatus*, *pCommand*, *Connection*, *pConnection*

## <a name="parameters"></a>Paramètres

  - *RecordsAffected*

  - Valeur de type **Long** indiquant le nombre d'enregistrements affectés par la commande.

  - *pError*

  - Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si **adStatus** a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Avant que cet événement soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre pour éviter toute notification ultérieure.

  - *pCommand*

  - L’objet [Command](command-object-ado.md) qui a été exécutée. Contient un objet **Command** même lors de l’appel de **méthode Connection.Execute** ou **Recordset.Open** sans création explicite d’une **commande**dans les cas de l’objet **Command** est créée en interne par ADO.

  - *Connection*

  - Objet [Recordset](recordset-object-ado.md) résultant de la commande exécutée. Cet objet **Recordset** peut être vide. Il ne doit jamais être détruit à partir de ce gestionnaire d'événements. En effet, cela entraîne une violation d'accès puisqu'ADO tente d'accéder à un objet qui n'existe plus.

  - *pConnection*

  - Objet [Connection](connection-object-ado.md), représentant la connexion utilisée pour l'exécution de l'opération.

## <a name="remarks"></a>Notes

Un événement **ExecuteComplete** peut se produire avec les méthodes **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.**[Open](open-method-ado-recordset.md), **Recordset.**[Requery](requery-method-ado.md) ou **Recordset.**[NextRecordset](nextrecordset-method-ado.md).

