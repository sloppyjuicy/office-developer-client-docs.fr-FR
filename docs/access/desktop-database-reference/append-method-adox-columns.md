---
title: Append, méthode (Colonnes ADOX)
TOCTitle: Append Method (ADOX Columns)
ms:assetid: e256a478-abc0-f15b-fc29-1b52e354144a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250152(v=office.15)
ms:contentKeyID: 48548285
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f64f3b04df989348173ad2fc975dcefbd1114b2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469553"
---
# <a name="append-method-adox-columns"></a>Append, méthode (Colonnes ADOX)


**S’applique à**: Access 2013 | Office 2013

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
> <P>[!REMARQUE] Une erreur survient lors de l'ajout d'une <STRONG>colonne</STRONG> à la collection <STRONG>Columns</STRONG> d'un <A href="index-object-adox.md">index</A> si la <STRONG>colonne</STRONG> n'existe pas dans une <A href="table-object-adox.md">table</A> déjà ajoutée à la collection <A href="tables-collection-adox.md">Tables</A>.</P>


