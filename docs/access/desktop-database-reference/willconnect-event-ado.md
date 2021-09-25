---
title: WillConnect, événement (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e223eebf5f3fa6c9b4780c6d52fbe41b22b42d5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588587"
---
# <a name="willconnect-event-ado"></a>WillConnect, événement (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **WillConnect** est appelé avant le début d'une connexion.

## <a name="syntax"></a>Syntaxe

WillConnect *ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*ConnectionString* |Valeur de type **String** contenant les informations de la connexion en attente.|
|*UserID* |Valeur de type **String** reprenant le nom de l'utilisateur de la connexion en attente.|
|*Password* |Valeur de type **String** contenant un mot de passe pour la connexion en attente.|
|*Options* |Valeur de type **Long** indiquant la méthode d'évaluation du paramètre *ConnectionString* par le fournisseur. La seule option possible est **adAsyncOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque cet événement est appelé, ce paramètre est défini à **adStatusOK** par défaut. Il est défini à **adStatusCantDeny** si l'événement ne peut pas demander l'annulation de l'opération en attente.<br/><br/>Avant que cet événement soit retourné, affectez au paramètre la valeur **adStatusUnwantedEvent** pour éviter toute notification ultérieure ou la valeur **adStatusCancel** pour demander l'opération de connexion provoquant l'annulation de cette notification.|
|*pConnection* |Objet [Connection](connection-object-ado.md) auquel cette notification d'événement s'applique. Les modifications apportées aux paramètres de l'objet **Connection** par le gestionnaire d'événements **WillConnect** n'ont aucun effet sur l'objet **Connection**.|

## <a name="remarks"></a>Remarques

Si **WillConnect** est appelé, les paramètres *ConnectionString*, *UserID*, *Password* et *Options* prennent les valeurs établies par l'opération à l'origine de l'événement (à savoir, la connexion en attente) et ne peuvent pas être modifiés tant que l'événement n'est pas retourné. Il se peut que le gestionnaire d'événements **WillConnect** renvoie une demande d'annulation de la connexion en attente.

Si c'est le cas, **ConnectComplete** est alors appelé et son paramètre *adStatus* est affecté de la valeur **adStatusErrorsOccurred**.

