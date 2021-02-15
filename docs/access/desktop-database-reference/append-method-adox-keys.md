---
title: Append, méthode (Clés ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c301f6809ab7f785497637b12e0b5d7a0bb7772d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297087"
---
# <a name="append-method-adox-keys"></a>Append, méthode (Clés ADOX)

**S’applique à** : Access 2013, Office 2013

Ajoute un nouvel objet [Key](key-object-adox.md) à la collection [Keys](keys-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Touches*. Touche *d’append* \[ ,*KeyType* \] \[ ,*Colonne* \] \[ ,*RelatedTable* \] \[ ,*RelatedColumn*\]

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Key* |Objet **Key** à ajouter ou nom de la clé à créer et à ajouter.|
|*KeyType* |Facultatif. Valeur de type **Long** qui spécifie le type de clé. Le paramètre *Key* correspond à la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) d’un objet **Key**.|
|*Colonne* |Facultatif. Valeur de type **String** qui spécifie le nom de la colonne à indexer. Le paramètre *Columns* correspond à la valeur de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md).|
|*RelatedTable* |Facultatif. Valeur de type **String** qui spécifie le nom de la table liée. Le paramètre *RelatedTable* correspond à la valeur de la propriété **Name** d’un objet [Table](table-object-adox.md).|
|*RelatedColumn* |Facultatif. Valeur de type **String** qui spécifie le nom de la colonne liée pour une clé étrangère. Le paramètre RelatedColumn correspond à la valeur de la propriété **Name** d'un objet **Column**.|

## <a name="remarks"></a>Remarques

Le paramètre *Columns* peut prendre soit le nom d'une colonne, soit une matrice de noms de colonne.

