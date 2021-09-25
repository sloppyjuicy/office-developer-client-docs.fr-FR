---
title: Delete, méthode (collection Fields ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 463056a45ce3636d6b215c03fd65e8614f633bf3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577443"
---
# <a name="delete-method-ado-fields-collection"></a>Delete, méthode (collection Fields ADO)

**S’applique à** : Access 2013, Office 2013


Supprime un objet de la collection [Fields](fields-collection-ado.md).

## <a name="syntax"></a>Syntaxe

*Champs*. Supprimer un *champ*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Field* |A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.|

## <a name="remarks"></a>Remarques

L’appel de la méthode **Fields.Delete** sur un objet [Recordset](recordset-object-ado.md) ouvert provoque un erreur d’exécution.

