---
title: WillConnect, événement (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703432"
---
# <a name="willconnect-event-ado"></a>WillConnect, événement (ADO)

**S’applique à**: Access 2013, Office 2013

L'événement **WillConnect** est appelé avant le début d'une connexion.

## <a name="syntax"></a>Syntaxe

WillConnect*ConnectionString*, *UserID*, *le mot de passe*, *Options*, *adStatus*, *pConnection*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*ConnectionString* |Valeur de type **String** contenant les informations de la connexion en attente.|
|*UserID* |Valeur de type **String** reprenant le nom de l'utilisateur de la connexion en attente.|
|*Password* |Valeur de type **String** contenant un mot de passe pour la connexion en attente.|
|*Options* |Valeur de type **Long** indiquant la méthode d'évaluation du paramètre *ConnectionString* par le fournisseur. La seule option possible est **adAsyncOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque cet événement est appelé, ce paramètre est défini à **adStatusOK** par défaut. Il est défini à **adStatusCantDeny** si l'événement ne peut pas demander l'annulation de l'opération en attente.<br/><br/>Avant que cet événement soit retourné, affectez au paramètre la valeur **adStatusUnwantedEvent** pour éviter toute notification ultérieure ou la valeur **adStatusCancel** pour demander l'opération de connexion provoquant l'annulation de cette notification.|
|*pConnection* |Objet [Connection](connection-object-ado.md) auquel cette notification d'événement s'applique. Les modifications apportées aux paramètres de l'objet **Connection** par le gestionnaire d'événements **WillConnect** n'ont aucun effet sur l'objet **Connection**.|

## <a name="remarks"></a>Notes

Si **WillConnect** est appelé, les paramètres *ConnectionString*, *UserID*, *Password* et *Options* prennent les valeurs établies par l'opération à l'origine de l'événement (à savoir, la connexion en attente) et ne peuvent pas être modifiés tant que l'événement n'est pas retourné. Il se peut que le gestionnaire d'événements **WillConnect** renvoie une demande d'annulation de la connexion en attente.

Lorsque cet événement est annulé, **ConnectComplete** est alors appelé et son paramètre *adStatus* la valeur **adStatusErrorsOccurred**.

