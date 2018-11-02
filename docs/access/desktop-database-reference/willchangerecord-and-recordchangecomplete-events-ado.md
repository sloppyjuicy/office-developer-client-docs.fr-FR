---
title: WillChangeRecord et RecordChangeComplete, événements (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3177e27d3485d8a4ec6adafaa03d968fc15fa62a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925958"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>WillChangeRecord et RecordChangeComplete, événements (ADO)


**S’applique à**: Access 2013, Office 2013


L'événement **WillChangeRecord** est appelé avant qu'un ou plusieurs enregistrements (lignes) de l'objet [Recordset](recordset-object-ado.md) soient modifiés. À l'inverse, l'événement **RecordChangeComplete** est appelé après la modification d'enregistrements.

## <a name="syntax"></a>Syntaxe

WillChangeRecord*adReason*, *cRecords*, *adStatus*, *Connection*

RecordChangeComplete*adReason*, *cRecords*, *pError*, *adStatus*, *Connection*

## <a name="parameters"></a>Paramètres

  - *adReason*

  - Valeur [EventReasonEnum](eventreasonenum.md) indiquant la raison de cet événement. Les valeurs possibles sont **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete** et **adRsnFirstChange**.

  - *cRecords*

  - Valeur de type **Long** indiquant le nombre d'enregistrements en cours de modification (c'est-à-dire affectés par l'opération).

  - *pError*

  - Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.

  - *adStatus*

  - [EventStatusEnum](eventstatusenum.md)
    
    Lorsque **WillChangerecord** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente.
    
    Lorsque **RecordChangeComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué.
    
    Avant que **WillChangeRecord** soit retourné, définissez ce paramètre à **adStatusCancel** pour demander l'annulation de l'opération à l'origine de l'événement ou à adStatusUnwantedEvent pour éviter toute notification ultérieure.
    
    Avant que **RecordChangeComplete** soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure.

  - *Connection*

  - Objet **Recordset**. Le **jeu d’enregistrements** pour laquelle cet événement se produit.

## <a name="remarks"></a>Notes

Il se peut qu'un événement **WillChangeRecord** ou **RecordChangeComplete** se produise pour le premier champ modifié dans une ligne lorsque les opérations suivantes sont effectuées sur l'objet **Recordset**: [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) et [CancelBatch](cancelbatch-method-ado.md). La valeur de l' **objet Recordset** [CursorType](cursortype-property-ado.md) détermine les opérations qui déclenchent les événements.

Pendant l’événement **WillChangeRecord** , la propriété [Filter](filter-property-ado.md) de **jeu d’enregistrements** est définie à **adFilterAffectedRecords**. Sa valeur n'est pas modifiable lorsque l'événement est en cours de traitement.

Vous devez affecter la valeur adStatusUnwantedEvent au paramètre adStatus pour chaque valeur possible du paramètre adReason afin d'empêcher définitivement les notifications des événements comprenant un paramètre adReason.

