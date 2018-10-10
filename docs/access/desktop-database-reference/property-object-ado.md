---
title: Property, objet (ADO)
TOCTitle: Property Object (ADO)
ms:assetid: eec318fd-f5ed-d9ef-9830-848439a8914d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250210(v=office.15)
ms:contentKeyID: 48548567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b3cb4d5caedb6e73bf0819639c1feac12b9d3a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469501"
---
# <a name="property-object-ado"></a>Property, objet (ADO)


**S’applique à**: Access 2013 | Office 2013

Représente une caractéristique dynamique d'un objet ADO défini par le fournisseur.

## <a name="remarks"></a>Notes

Les objets ADO possèdent deux types de propriétés : intégrées et dynamiques.

Les propriétés intégrées sont les propriétés implémentées dans ADO et immédiatement disponibles pour tout nouvel objet, en utilisant la syntaxe. Elles n'apparaissent pas en tant qu'objets **Property** dans une collection [Properties](properties-collection-ado.md) d'un objet ; ainsi, même si vous pouvez modifier leurs valeurs, vous ne pouvez pas modifier leurs caractéristiques.

Les propriétés dynamiques sont définies par le fournisseur de données sous-jacent et apparaissent dans la collection **Properties** de l'objet ADO correspondant. Par exemple, une propriété spécifique au fournisseur peut indiquer si un objet [Recordset](recordset-object-ado.md) prend en charge les transactions ou les mises à jour. Ces propriétés supplémentaires apparaissent comme des objets **Property** dans la collection **Properties** de cet objet **Recordset**. Propriétés dynamiques peuvent être référencées seulement par le biais de la collection à l’aide de la MyObject.Properties(0) ou ou MyObject.Properties("Name").

Vous ne pouvez supprimer l'une ou l'autre propriété.

Un objet **Property** dynamique comporte quatre propriétés intégrées :

  - La propriété [Name](name-property-ado.md) est une chaîne qui identifie la propriété.

  - La propriété [Type](type-property-ado.md) est un entier qui spécifie le type de données de la propriété.

  - Sa propriété [Value](value-property-ado.md) est une variante qui contient le paramètre de la propriété. **Value** est la propriété par défaut d'un objet **Property**.

  - Sa propriété [Attributes](attributes-property-ado.md) est une valeur de type long qui indique les caractéristiques de la propriété spécifiques du fournisseur.

