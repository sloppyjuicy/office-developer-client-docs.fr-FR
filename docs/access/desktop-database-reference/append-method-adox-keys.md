---
title: Append, méthode (Clés ADOX)
TOCTitle: Append Method (ADOX Keys)
ms:assetid: 14d6e8d7-5c9e-a422-47d6-ebfd9dd7a120
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248913(v=office.15)
ms:contentKeyID: 48543396
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d7e10e272155d2d0377810bf8aa1704a30bad39
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471978"
---
# <a name="append-method-adox-keys"></a>Append, méthode (Clés ADOX)


**S’applique à**: Access 2013 | Office 2013


Ajoute un nouvel objet [Key](key-object-adox.md) à la collection [Keys](keys-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Clés*. Ajoutez la*clé* \[,*type de clé* \] \[,*colonne* \] \[,*RelatedTable* \] \[,*RelatedColumn*\]

## <a name="parameters"></a>Paramètres

  - *Key*

  - Objet **Key** à ajouter ou nom de la clé à créer et à ajouter.

  - *Type de clé*

  - Facultatif. Valeur de type **Long** qui spécifie le type de clé. Le paramètre de *clé* correspond à la propriété [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) d’un objet **Key** .

  - *Column*

  - Facultatif. Valeur de type **String** qui spécifie le nom de la colonne à indexer. Le paramètre *Columns* correspond à la valeur de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md) .

  - *RelatedTable*

  - Facultatif. Valeur de type **String** qui spécifie le nom de la table liée. Le paramètre *RelatedTable* correspond à la valeur de la propriété **Name** d’un objet [Table](table-object-adox.md) .

  - *RelatedColumn*

  - Facultatif. Valeur de type **String** qui spécifie le nom de la colonne liée pour une clé étrangère. Le paramètre RelatedColumn correspond à la valeur de la propriété **Name** d'un objet **Column**.

## <a name="remarks"></a>Notes

Le paramètre *Columns* peut prendre soit le nom d’une colonne ou un tableau de noms de colonne.

