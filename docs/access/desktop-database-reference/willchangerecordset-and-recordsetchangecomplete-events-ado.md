---
title: WillChangeRecordset et RecordsetChangeComplete, événements (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfb304f41ada88e1b0546aaa4a54240b931017cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302820"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>WillChangeRecordset et RecordsetChangeComplete, événements (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **WillChangeRecordset** est appelé avant qu'une opération en attente modifie l'objet [Recordset](recordset-object-ado.md). À l’inverse, l’événement **RecordsetChangeComplete** est appelé après cette modification de l’objet **Recordset**.

## <a name="syntax"></a>Syntaxe

WillChangeRecordset *adReason*, *adStatus*, *pRecordset*

RecordsetChangeComplete *adReason*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*adReason* |Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnRequery**, **adRsnResynch**, **adRsnClose** et **adRsnOpen**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **WillChangeRecordset** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente. <br/><br/>Lorsque **RecordsetChangeComplete** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement, à **adStatusErrorsOccurred** si cette dernière a échoué ou encore à **adStatusCancel** si l'opération associée à l'événement **WillChangeRecordset** précédemment accepté a été annulée <br/><br/>Avant que **WillChangeRecordset** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération en attente ou à adStatusUnwantedEvent pour éviter toute notification ultérieure. <br/><br/>Avant que **WillChangeRecordset** ou que **RecordsetChangeComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*pRecordset* |A **Recordset** object. The **Recordset** for which this event occurred.|

## <a name="remarks"></a>Remarques

Un **événement WillChangeRecordset** ou **RecordsetChangeComplete** peut se produire en raison des méthodes [Requery](requery-method-ado.md) ou [Open](open-method-ado-recordset.md) du jeu d’enregistrements. 

Si le fournisseur ne prend pas en charge les signets, une notification d'événement **RecordsetChange** est générée chaque fois que des nouvelles lignes sont extraites du fournisseur. La fréquence de cet événement dépend de la propriété **RecordsetCacheSize**.

Vous devez affecter au paramètre **adStatus** la valeur **adStatusUnwantedEvent** pour chaque valeur possible du paramètre **adReason** afin d'empêcher définitivement les notifications des événements comprenant un paramètre **adReason**.

