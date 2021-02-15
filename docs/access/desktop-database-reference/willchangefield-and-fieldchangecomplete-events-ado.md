---
title: WillChangeField et FieldChangeComplete, événements (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302484"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>WillChangeField et FieldChangeComplete, événements (ADO)

**S’applique à** : Access 2013, Office 2013

L'événement **WillChangeField** est appelé avant qu'une opération en attente modifie la valeur d'objets [Field](field-object-ado.md) dans l'objet [Recordset](recordset-object-ado.md). Quant à l'événement **FieldChangeComplete**, il est appelé après la modification de la valeur d'un ou plusieurs objets **Field**.

## <a name="syntax"></a>Syntaxe

WillChangeField *cFields*, *Fields*, *adStatus*, *pRecordset*

FieldChangeComplete *cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*cFields* |Valeur de type **Long** indiquant le nombre d'objets **Field** inclus dans *Fields*.|
|*Fields* |Dans le cas de **WillChangeField**, le paramètre *Fields* correspond à un tableau de valeurs de type **Variant** qui contient des objets **Field** avec les valeurs d'origine. <br/><br/>
En ce qui concerne **FieldChangeComplete**, le paramètre *Fields* correspond à un tableau de valeurs de type **Variant** qui contient des objets **Field** avec les valeurs modifiées.|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **WillChangeField** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente. <br/><br/>Lorsque **FieldChangeComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué. <br/><br/>Avant que **WillChangeField** ne soit retourné, affectez la valeur **adStatusCancel** à ce paramètre pour demander l'annulation de l'opération en attente. <br/><br/>Avant que **FieldChangeComplete** ne soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre afin d'empêcher toute notification ultérieure.|
|*pRecordset* |A **Recordset** object. The **Recordset** for which this event occurred.|

## <a name="remarks"></a>Remarques

Un événement **WillChangeField** ou **FieldChangeComplete** est parfois généré lorsque vous définissez la propriété [Value](value-property-ado.md) et que vous appelez la méthode [Update](update-method-ado.md) à l’aide des paramètres de tableau de champs et de valeurs.

