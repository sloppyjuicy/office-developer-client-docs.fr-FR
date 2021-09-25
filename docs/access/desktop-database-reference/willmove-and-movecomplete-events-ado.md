---
title: WillMove et MoveComplete, événements (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b61fc2affe707b03b5415acd1777fbf0b7dc750e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585038"
---
# <a name="willmove-and-movecomplete-events-ado"></a>WillMove et MoveComplete, événements (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **WillMove** est appelé avant qu'une opération en attente modifie la position active dans l'objet [Recordset](recordset-object-ado.md). À l'inverse, l'événement **MoveComplete** est appelé après la modification de la position active dans l'objet **Recordset**.

## <a name="syntax"></a>Syntaxe

WillMove *adReason*, *adStatus*, *pRecordset*

MoveComplete *adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*adReason* |Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnMoveFirst**, **adRsnMoveLast**, **adRsnMoveNext**, **adRsnMovePrevious**, **adRsnMove** et **adRsnRequery**.|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **WillMove** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente. <br/><br/>Lorsque **MoveComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué. <br/><br/>Avant que **WillMove** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération en attente ou à adStatusUnwantedEvent pour éviter toute notification ultérieure. <br/><br/>Avant que **MoveComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.|
|*pRecordset* |A [Recordset](recordset-object-ado.md) object. The **Recordset** for which this event occurred.|

## <a name="remarks"></a>Remarques

Un **événement WillMove** ou **MoveComplete** peut se produire en raison des opérations **recordset suivantes** :

- [Ouvert](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Actualiser](requery-method-ado.md)

Ces événements peuvent se produire en raison des propriétés suivantes :

- [Filtre](filter-property-ado.md)
- [Index](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Ils sont également générés si un objet **Recordset** enfant possède des événements relatifs à **Recordset** et que l'objet **Recordset** parent est déplacé.

Vous devez affecter au paramètre *adStatus* la valeur **adStatusUnwantedEvent** pour chaque valeur possible du paramètre *adReason* afin d'empêcher définitivement les notifications des événements comprenant un paramètre *adReason*.

