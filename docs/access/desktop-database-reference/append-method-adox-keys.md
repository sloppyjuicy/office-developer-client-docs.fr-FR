---
title: Append, méthode (Clés ADOX)
TOCTitle: Append method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d99af00f1ad83087994737f5bb3ca29acf2a9deb
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949816"
---
# <a name="append-method-adox-keys"></a>Append, méthode (Clés ADOX)

**S’applique à**: Access 2013, Office 2013

Ajoute un nouvel objet [Key](key-object-adox.md) à la collection [Keys](keys-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Clés*. Ajoutez la*clé* \[,*type de clé* \] \[,*colonne* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Key* |Objet **Key** à ajouter ou nom de la clé à créer et à ajouter.|
|*Type de clé* |Facultatif. Valeur de type **Long** qui spécifie le type de clé. Le paramètre de *clé* correspond à la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) d’un objet **Key** .|
|*Column* |Facultatif. Valeur de type **String** qui spécifie le nom de la colonne à indexer. Le paramètre *Columns* correspond à la valeur de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md) .|
|*RelatedTable* |Facultatif. Valeur de type **String** qui spécifie le nom de la table liée. Le paramètre *RelatedTable* correspond à la valeur de la propriété **Name** d’un objet [Table](table-object-adox.md) .|
|*RelatedColumn* |Facultatif. Valeur de type **String** qui spécifie le nom de la colonne liée pour une clé étrangère. Le paramètre RelatedColumn correspond à la valeur de la propriété **Name** d'un objet **Column**.|

## <a name="remarks"></a>Notes

Le paramètre *Columns* peut prendre soit le nom d’une colonne ou un tableau de noms de colonne.

