---
title: Objet Axis (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 057fa3c22c399f6f573a3ee2028cd7a80d8ad937
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602919"
---
# <a name="axis-object-ado-md"></a>Objet Axis (ADO MD)


**S’applique à** : Access 2013, Office 2013

Représente un axe de position ou de filtrage d'un ensemble de cellules, contenant des membres sélectionnés d'une ou plusieurs dimensions.

## <a name="remarks"></a>Remarques

Un objet **Axis** peut faire partie d’une collection [Axes](axes-collection-ado-md.md) ou être renvoyé par la propriété [FilterAxis](filteraxis-property-ado-md.md) d’un [ensemble de cellules](cellset-object-ado-md.md).

Avec les collections et propriétés d'un objet **Axis**, vous pouvez :

- Identifier l' **axe** à l'aide de la propriété [Name](name-property-ado-md.md).

- Parcourir chaque position le long d'un **axe** à l'aide de la collection [Positions](positions-collection-ado-md.md).

- Obtenir le nombre de dimensions sur l' **axe** à l'aide de la propriété [DimensionCount](dimensioncount-property-ado-md.md).

- Obtenir les attributs spécifiques au fournisseur de l' **axe** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).

