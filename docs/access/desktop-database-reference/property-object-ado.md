---
title: Property, objet (ADO)
TOCTitle: Property object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 262f4873359508a985b27f3d4ea70a5fcbfd620f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302918"
---
# <a name="property-object-ado"></a>Property, objet (ADO)


**S’applique à** : Access 2013, Office 2013

Représente une caractéristique dynamique d'un objet ADO défini par le fournisseur.

## <a name="remarks"></a>Remarques

Les objets ADO possèdent deux types de propriétés : intégrées et dynamiques.

Les propriétés intégrées sont les propriétés implémentées dans ADO et immédiatement disponibles pour tout nouvel objet, à l'aide de la syntaxe. Elles n'apparaissent pas en tant qu'objets **Property** dans une collection [Properties](properties-collection-ado.md) d'un objet ; ainsi, même si vous pouvez modifier leurs valeurs, vous ne pouvez pas modifier leurs caractéristiques.

Les propriétés dynamiques sont définies par le fournisseur de données sous-jacent et apparaissent dans la collection **Properties** de l'objet ADO correspondant. Par exemple, une propriété spécifique au fournisseur peut indiquer si un objet [Recordset](recordset-object-ado.md) prend en charge les transactions ou les mises à jour. Ces propriétés supplémentaires apparaissent comme des objets **Property** dans la collection **Properties** de cet objet **Recordset**. Les propriétés dynamiques peuvent être référencées uniquement via la collection, à l'aide de la syntaxe MyObject. Properties (0) ou MyObject. Properties ("nom").

Vous ne pouvez supprimer ni l'un ni l'autre de ces deux types de propriétés.

Un objet **Property** dynamique possède quatre propriétés intégrées :

  - Sa propriété [Name](name-property-ado.md) est une chaîne qui identifie la propriété.

  - Sa propriété [Type](type-property-ado.md) est un entier qui spécifie le type de données de la propriété.

  - Sa propriété [Value](value-property-ado.md) est une variante qui contient le paramètre de la propriété. **Value** est la propriété par défaut d'un objet **Property**.

  - Sa propriété [Attributes](attributes-property-ado.md) est une valeur de type long qui indique les caractéristiques de la propriété spécifiques du fournisseur.

