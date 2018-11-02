---
title: Catalog, objet (ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b977db2faf07a47c2e9234cec4a7828def5e6188
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926737"
---
# <a name="catalog-object-ado-md"></a>Catalog, objet (ADO MD)


**S’applique à**: Access 2013, Office 2013

Contient les informations de schéma multidimensionnel (en d'autres termes, les cubes et dimensions sous-jacentes, les hiérarchies, les niveaux et les membres) spécifiques à un fournisseur de données multidimensionnelles (MDP).

## <a name="remarks"></a>Remarques

Avec les collections et propriétés d'un objet **Catalog**, vous pouvez :

  - Ouvrir le catalogue en définissant la propriété [ActiveConnection](activeconnection-property-ado-md.md) sur un objet ADO [Connection](connection-object-ado.md) standard ou une chaîne de connexion valide.

  - Identifier le **catalogue** à l'aide de la propriété [Name](name-property-ado-md.md).

  - Parcourir les cubes d'un catalogue à l'aide de la collection [CubeDefs](cubedefs-collection-ado-md.md).

