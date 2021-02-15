---
title: WillChangeRecord et RecordChangeComplete, événements (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0113a7b22d0bba8e843ce9583e93eef848f872a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305984"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>WillChangeRecord et RecordChangeComplete, événements (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **WillChangeRecord** est appelé avant qu'un ou plusieurs enregistrements (lignes) de l'objet [Recordset](recordset-object-ado.md) soient modifiés. À l'inverse, l'événement **RecordChangeComplete** est appelé après la modification d'enregistrements.

## <a name="syntax"></a>Syntaxe

WillChangeRecord *adReason*, *cRecords*, *adStatus*, *pRecordset*

RecordChangeComplete *adReason*, *cRecords*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*adReason* |Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** et **adRsnFirstChange**.|
|*cRecords* |Valeur de type **Long** indiquant le nombre d'enregistrements en cours de modification (c'est-à-dire affectés par l'opération).|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **WillChangerecord** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente. <br/><br/>Lorsque **RecordChangeComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué. <br/><br/>Avant que **WillChangeRecord** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération à l'origine de l'événement ou à adStatusUnwantedEvent pour éviter toute notification ultérieure. <br/><br/>Avant que **RecordChangeComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.|
|*pRecordset* |A **Recordset** object. The **Recordset** for which this event occurred.|

## <a name="remarks"></a>Remarques

Il se peut qu'un événement **WillChangeRecord** ou **RecordChangeComplete** se produise pour le premier champ modifié dans une ligne lorsque les opérations suivantes sont effectuées sur l'objet **Recordset**: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) et [CancelBatch](cancelbatch-method-ado.md). La valeur du type [CursorType](cursortype-property-ado.md) du jeu d’enregistrements détermine les opérations à l’origine des événements. 

Pendant **l’événement WillChangeRecord,** la propriété **Recordset** [Filter](filter-property-ado.md) est définie sur **adFilterAffectedRecords**. Sa valeur n'est pas modifiable lorsque l'événement est en cours de traitement.

Vous devez affecter la valeur adStatusUnwantedEvent au paramètre adStatus pour chaque valeur possible du paramètre adReason afin d'empêcher définitivement les notifications des événements comprenant un paramètre adReason.

