---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec64241bf63719fe4f5c547d60a93f7804f181ca
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877659"
---
# <a name="append-method-adox-columns"></a>Append, méthode (Colonnes ADOX)


**S’applique à**: Access 2013, Office 2013

Ajoute un nouvel objet [Column](column-object-adox.md) à la collection [Columns](columns-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Colonnes*. Ajouter la*colonne* \[,*Type* \] \[,*DefinedSize*\]

## <a name="parameters"></a>Paramètres

  - *Column*

  - Objet **Column** à ajouter ou nom de la colonne à créer et à ajouter.

  - *Type*

  - Facultatif. Valeur de type **long** qui spécifie le type de données de la colonne. Le paramètre *Type* correspond à la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) d’un objet **Column** .

  - *DefinedSize*

  - Facultatif. Valeur de type **long** qui spécifie la taille de la colonne. Le paramètre *DefinedSize* correspond à la propriété [DefinedSize](definedsize-property-adox.md) d’un objet **Column** .


> [!NOTE]
> [!REMARQUE] Une erreur survient lors de l'ajout d'une **colonne** à la collection **Columns** d'un [index](index-object-adox.md) si la **colonne** n'existe pas dans une [table](table-object-adox.md) déjà ajoutée à la collection [Tables](tables-collection-adox.md).


