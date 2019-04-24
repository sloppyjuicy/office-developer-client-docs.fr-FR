---
title: Événement WillExecute, (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe15604d0160afcbde5fdf02eaa6a7831da874b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302754"
---
# <a name="willexecute-event-ado"></a>Événement WillExecute, (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **WillExecute** est appelé juste avant l'exécution d'une commande en attente sur une connexion.

## <a name="syntax"></a>Syntaxe

*Source*WillExecute,, *CursorType*, *LockType*, *options*, ** adStatus, *pCommand*, preobjet, *pConnection* **

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*Source* |Valeur de type **String** reprenant le nom d'une commande SQL ou d'une procédure stockée.|
|*CursorType* |Valeur [CursorTypeEnum](cursortypeenum.md) contenant le type de curseur pour l'objet **Recordset** qui sera ouvert. Avec ce paramètre, vous pouvez modifier le type de curseur pendant l'opération d' [ouverture](open-method-ado-recordset.md) **d'un jeu d'enregistrements** . La valeur du paramètre *CursorType* est ignorée pour tout autre type d’opération.|
|*LockType* |Valeur [LockTypeEnum](locktypeenum.md) contenant le type de verrouillage de l'objet **Recordset** qui sera ouvert. Ce paramètre permet de changer le type de verrouillage pendant l'exécution d'une opération **Open** sur un objet **Recordset** ). La valeur de *LockType* est ignorée pour tout autre type d’opération.|
|*Options* |Valeur de type **Long** indiquant les options qui peuvent être utilisées pour exécuter la commande ou ouvrir l'objet **Recordset**.|
|*Statu* |[EventStatusEnum](eventstatusenum.md). Avant que cet événement soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure ou à **adStatusCancel** pour demander l'annulation de l'opération à l'origine de l'événement.|
|*pCommand* |Objet [Command](command-object-ado.md) auquel cette notification d'événement s'applique.|
|*jeu d'enregistrements* |Objet [Recordset](recordset-object-ado.md) auquel cette notification d'événement s'applique.|
|*pConnection* |Objet [Connection](connection-object-ado.md) auquel cette notification d'événement s'applique.|

## <a name="remarks"></a>Remarques

Il se peut qu’un événement **WillExecute** se produise suite à l’utilisation de la méthode **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) ou **Recordset.**[Open](open-method-ado-recordset.md). Le paramètre *pConnection* doit toujours contenir une référence valide à un objet **Connection**. Si l’événement est lié à l’exécution de **Connection.Execute**, les paramètres *pRecordset* et *pCommand* ont la valeur **Nothing**. S’il est provoqué par la méthode **Recordset.Open**, le paramètre *pRecordset* fait alors référence à l’objet **Recordset** et le paramètre *pCommand* est défini  **Nothing**. Enfin, si l’événement est provoqué par la méthode **Command.Execute**, le paramètre *pCommand* fait alors référence à l’objet **Command** et le paramètre *pRecordset* a la valeur **Nothing**.

**WillExecute** permet de passer en revue et de modifier les paramètres d'exécution en attente. Il se peut que cet événement retourne une demande d'annulation de la commande en attente.

