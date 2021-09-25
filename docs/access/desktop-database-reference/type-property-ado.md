---
title: Type, propriété (ADO)
TOCTitle: Type property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f8bcdfe1c5f3ea1890603ef3c5b69258d3140ca6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585115"
---
# <a name="type-property-ado"></a>Type, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le type opérationnel ou le type de données de l'objet [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Remarques

La propriété **Type** est en lecture/écriture pour les objets **Parameter**. Pour les nouveaux objets **Field** ayant été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Type** n'est accessible en lecture et en écriture qu'une fois que la propriété [Value](value-property-ado.md) de l'objet **Field** est spécifiée et que le fournisseur de données a correctement ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.

Pour tous les autres objets, la propriété **Type** est en lecture seule.

