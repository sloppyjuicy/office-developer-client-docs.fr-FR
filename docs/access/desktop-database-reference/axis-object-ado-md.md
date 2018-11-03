---
title: Axis, objet (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e90ff31c0b6a78a3f242927e2fa7e84c42d6ab3
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945347"
---
# <a name="axis-object-ado-md"></a>Axis, objet (ADO MD)


**S’applique à**: Access 2013, Office 2013

Représente un axe de position ou de filtrage d'un ensemble de cellules, contenant des membres sélectionnés d'une ou plusieurs dimensions.

## <a name="remarks"></a>Remarques

Un objet **Axis** peut faire partie d'une collection [Axes](axes-collection-ado-md.md) ou être renvoyé par la propriété [FilterAxis](filteraxis-property-ado-md.md) d'un [ensemble de cellules](cellset-object-ado-md.md).

Avec les collections et propriétés d'un objet **Axis**, vous pouvez :

- Identifier l' **axe** à l'aide de la propriété [Name](name-property-ado-md.md).

- Parcourir chaque position le long d'un **axe** à l'aide de la collection [Positions](positions-collection-ado-md.md).

- Obtenir le nombre de dimensions sur l' **axe** à l'aide de la propriété [DimensionCount](dimensioncount-property-ado-md.md).

- Obtenir les attributs spécifiques au fournisseur de l' **axe** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).

