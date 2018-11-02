---
title: Append, méthode (Index ADOX)
TOCTitle: Append method (ADOX Indexes)
ms:assetid: 015ebab4-5e9d-8777-ac82-4d20e957c274
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248784(v=office.15)
ms:contentKeyID: 48542933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41eb1cc67dd5a2058f9c5673db381f0bc9067454
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921480"
---
# <a name="append-method-adox-indexes"></a>Append, méthode (Index ADOX)


**S’applique à**: Access 2013, Office 2013



Ajoute un nouvel objet [Index](index-object-adox.md) à la collection [Indexes](indexes-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Index*. Ajouter des*Index* \[,*colonnes*\]

## <a name="parameters"></a>Paramètres

  - *Index*

  - Objet **Index** à ajouter ou nom de l'index à créer et à ajouter.

  - *Columns*

  - Facultatif. Valeur de type **Variant** qui spécifie le ou les noms des colonne à indexer. Le paramètre *Columns* correspond à l’ou les valeurs de la propriété [Name](name-property-adox.md) d’un objet [Column](column-object-adox.md) ou des objets.

## <a name="remarks"></a>Remarques

Le paramètre *Columns* peut prendre soit le nom d’une colonne ou un tableau de noms de colonne.

Une erreur se produit si le fournisseur ne prend pas en charge la création d'index.

