---
title: Type, propriété (ADO)
TOCTitle: Type Property (ADO)
ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15)
ms:contentKeyID: 48543397
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ac119b9582634e619455870c8a2e115f5e8dafa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469993"
---
# <a name="type-property-ado"></a>Type, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le type opérationnel ou le type de données de l'objet [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou renvoie une valeur [DataTypeEnum](datatypeenum.md).

## <a name="remarks"></a>Remarques

La propriété **Type** est en lecture/écriture pour les objets **Parameter**. Pour les nouveaux objets **Field** ayant été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Type** n'est accessible en lecture et en écriture qu'une fois que la propriété [Value](value-property-ado.md) de l'objet **Field** est spécifiée et que le fournisseur de données a correctement ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.

Pour tous les autres objets, la propriété **Type** est en lecture seule.

