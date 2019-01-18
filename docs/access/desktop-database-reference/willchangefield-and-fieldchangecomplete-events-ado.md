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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700184"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>WillChangeField et FieldChangeComplete, événements (ADO)

**S’applique à**: Access 2013, Office 2013

L'événement **WillChangeField** est appelé avant qu'une opération en attente modifie la valeur d'objets [Field](field-object-ado.md) dans l'objet [Recordset](recordset-object-ado.md). Quant à l'événement **FieldChangeComplete**, il est appelé après la modification de la valeur d'un ou plusieurs objets **Field**.

## <a name="syntax"></a>Syntaxe

WillChangeField*cFields*, *champs*, *adStatus*, *Connection*

FieldChangeComplete*cFields*, *champs*, *pError*, *adStatus*, *Connection*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*cFields* |Valeur de type **Long** indiquant le nombre d'objets **Field** inclus dans *Fields*.|
|*Fields* |Pour **WillChangeField**, le paramètre *Fields* est un tableau de **variantes** qui contient des objets **Field** avec les valeurs d’origine. <br/><br/>Pour **FieldChangeComplete**, le paramètre *Fields* est un tableau de **variantes** qui contient des objets **Field** avec les valeurs modifiées.|
|*pError* |Objet [Error](error-object-ado.md), décrivant l'erreur qui s'est produite si *adStatus* a la valeur **adStatusErrorsOccurred**. Dans le cas contraire, il n'est pas défini.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Lorsque **WillChangeField** est appelé, ce paramètre est défini à **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement. Il est défini à **adStatusCantDeny** si cet événement ne peut pas demander l'annulation de l'opération en attente. <br/><br/>Lorsque **FieldChangeComplete** est appelé, ce paramètre a la valeur **adStatusOK** si l'opération à l'origine de l'événement s'est déroulée correctement ou **adStatusErrorsOccurred** si cette dernière a échoué. <br/><br/>Avant que **WillChangeField** ne soit retourné, affectez la valeur **adStatusCancel** à ce paramètre pour demander l'annulation de l'opération en attente. <br/><br/>Avant que **FieldChangeComplete** ne soit retourné, affectez la valeur **adStatusUnwantedEvent** à ce paramètre afin d'empêcher toute notification ultérieure.|
|*Connection* |Objet **Recordset**. Le **jeu d’enregistrements** pour laquelle cet événement se produit.|

## <a name="remarks"></a>Notes

Un événement **WillChangeField** ou **FieldChangeComplete** est parfois généré lorsque vous définissez la propriété [Value](value-property-ado.md) et que vous appelez la méthode [Update](update-method-ado.md) à l'aide des paramètres de tableau de champs et de valeurs.

