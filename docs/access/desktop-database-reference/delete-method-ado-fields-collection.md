---
title: DELETE, méthode (Collection de champs ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718258"
---
# <a name="delete-method-ado-fields-collection"></a>DELETE, méthode (Collection de champs ADO)

**S’applique à**: Access 2013, Office 2013


Supprime un objet de la collection [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Syntaxe

*Champs*. Supprimer le*champ*

## <a name="parameters"></a>Parameters

|Paramètre|Description|
|:--------|:----------|
|*Field* |**Variant** qui désigne l’objet [Field](field-object-ado.md) à supprimer. Ce paramètre peut être le nom de l’objet **Field** ou la position ordinale de l’objet **Field** lui-même.|

## <a name="remarks"></a>Notes

L'appel de la méthode **Fields.Delete** sur un objet [Recordset](recordset-object-ado.md) ouvert provoque un erreur d'exécution.

