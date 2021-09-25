---
title: NumericScale, propriété (ADO)
TOCTitle: NumericScale property (ADO)
ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15)
ms:contentKeyID: 48544824
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 104bcb5b3396af107ece235cd925e5fe2d5c9739
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615206"
---
# <a name="numericscale-property-ado"></a>NumericScale, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique l'échelle des valeurs numériques possibles dans un objet [Parameter](parameter-object-ado.md) ou [Field](field-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Byte** qui indique le nombre de décimales que comporteront les valeurs numériques.

## <a name="remarks"></a>Remarques

Utilisez la propriété **NumericScale** pour déterminer combien de chiffres à droite de la virgule seront utilisés pour représenter les valeurs d'un objet **Parameter** ou **Field** numérique.

Pour les objets **Parameter**, la propriété **NumericScale** est accessible en lecture et écriture.

Pour un objet **Field**, **NumericScale** est généralement en lecture seule. Toutefois, pour les objets **Field** récemment ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), **NumericScale** est exceptionnellement accessible en lecture et en écriture après la définition de la propriété [Value](value-property-ado.md) de l'objet **Field** et une fois que le fournisseur de données a ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md)de la collection **Fields**.

