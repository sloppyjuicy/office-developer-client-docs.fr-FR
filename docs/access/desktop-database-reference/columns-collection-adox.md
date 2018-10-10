---
title: Columns, collection (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13f9a17d7dfcd9e621e4f4b1f1fcc03e88b4d832
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471900"
---
# <a name="columns-collection-adox"></a>Columns, collection (ADOX)


**S’applique à**: Access 2013 | Office 2013

Contient tous les objets de [colonne](column-object-adox.md) d'une table, d'un index ou d'une clé.

## <a name="remarks"></a>Remarques

La méthode [Append](append-method-adox-columns.md) d'une collection **Columns** est unique pour ADOX. Vous pouvez :

  - Ajouter une nouvelle colonne à la collection à l'aide de la méthode **Append**.

Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :

  - Accéder à une colonne de la collection à l'aide de la propriété [Item](item-property-ado.md).

  - Renvoyer le nombre de colonnes de la collection à l'aide de la propriété [Count](count-property-ado.md).

  - Supprimer une colonne de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).

  - Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).


> [!NOTE]
> <P>[!REMARQUE] Une erreur survient lors de l'ajout d'une <STRONG>colonne</STRONG> à la collection <STRONG>Columns</STRONG> d'un <A href="index-object-adox.md">index</A> si la <STRONG>colonne</STRONG> n'existe pas dans une <A href="table-object-adox.md">table</A> déjà ajoutée à la collection <A href="tables-collection-adox.md">Tables</A>.</P>


