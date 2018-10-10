---
title: Axis, objet (ADO MD)
TOCTitle: Axis Object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f978c5e6304e33ac67dfd4a669fe9155afb0b64d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469943"
---
# <a name="axis-object-ado-md"></a>Axis, objet (ADO MD)


**S’applique à**: Access 2013 | Office 2013

Représente un axe de position ou de filtrage d'un ensemble de cellules, contenant des membres sélectionnés d'une ou plusieurs dimensions.

## <a name="remarks"></a>Remarques

Un objet **Axis** peut faire partie d'une collection [Axes](axes-collection-ado-md.md) ou être renvoyé par la propriété [FilterAxis](filteraxis-property-ado-md.md) d'un [ensemble de cellules](cellset-object-ado-md.md).

Avec les collections et propriétés d'un objet **Axis**, vous pouvez :

  - Identifier l' **axe** à l'aide de la propriété [Name](name-property-ado-md.md).

  - Parcourir chaque position le long d'un **axe** à l'aide de la collection [Positions](positions-collection-ado-md.md).

  - Obtenir le nombre de dimensions sur l' **axe** à l'aide de la propriété [DimensionCount](dimensioncount-property-ado-md.md).

  - Obtenir les attributs spécifiques au fournisseur de l' **axe** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).

