---
title: WillExecute, événement (ADO)
TOCTitle: WillExecute Event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a5c739ffd408a1f53539c88a3bdc4169eb4cebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469420"
---
# <a name="willexecute-event-ado"></a>WillExecute, événement (ADO)


**S’applique à**: Access 2013 | Office 2013


L'événement **WillExecute** est appelé juste avant l'exécution d'une commande en attente sur une connexion.

## <a name="syntax"></a>Syntaxe

WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *Connection*, *pConnection*

## <a name="parameters"></a>Paramètres

  - *Source*

  - Valeur de type **String** reprenant le nom d'une commande SQL ou d'une procédure stockée.

  - *CursorType*

  - Valeur [CursorTypeEnum](cursortypeenum.md) contenant le type de curseur pour l'objet **Recordset** qui sera ouvert. Avec ce paramètre, vous pouvez modifier le curseur à n’importe quel type pendant une opération [d’ouverture](open-method-ado-recordset.md) de **jeu d’enregistrements** . *CursorType* est ignorée pour tout autre opération.

  - *LockType*

  - Valeur [LockTypeEnum](locktypeenum.md) contenant le type de verrouillage de l'objet **Recordset** qui sera ouvert. Ce paramètre permet de changer le type de verrouillage pendant l'exécution d'une opération **Open** sur un objet **Recordset** ). *LockType* est ignorée pour tout autre opération.

  - *Options*

  - Valeur de type **Long** indiquant les options qui peuvent être utilisées pour exécuter la commande ou ouvrir l'objet **Recordset**.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Avant que cet événement soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure ou à **adStatusCancel** pour demander l'annulation de l'opération à l'origine de l'événement.

  - *pCommand*

  - Objet [Command](command-object-ado.md) auquel cette notification d'événement s'applique.

  - *Connection*

  - Objet [Recordset](recordset-object-ado.md) auquel cette notification d'événement s'applique.

  - *pConnection*

  - Objet [Connection](connection-object-ado.md) auquel cette notification d'événement s'applique.

## <a name="remarks"></a>Notes

Un événement **WillExecute** peut se produire suite à une **connexion.** [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **commande.** [Exécuter](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), ou **Recordset.** La méthode [Open](open-method-ado-recordset.md) le paramètre *pConnection* doit toujours contenir une référence valide à un objet **Connection** . Si l’événement est en raison de **Connection.Execute**, les paramètres *pRecordset* et *pCommand* sont définies sur **Nothing**. Si l’événement est en raison de la **méthode Recordset.Open**, le paramètre *Connection* référence à l’objet **Recordset** et le paramètre *pCommand* est défini sur **Nothing**. Si l’événement est en raison de **Command.Execute**, le paramètre *pCommand fait* référence à l’objet **Command** et le paramètre *Connection* est défini sur **Nothing**.

**WillExecute** permet de passer en revue et de modifier les paramètres d'exécution en attente. Il se peut que cet événement retourne une demande d'annulation de la commande en attente.

