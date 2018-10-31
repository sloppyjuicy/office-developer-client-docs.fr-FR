---
title: Columns, collection (ADOX)
TOCTitle: Columns Collection (ADOX)
ms:assetid: 231645db-70da-9ad1-fb27-02145ce32e66
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249008(v=office.15)
ms:contentKeyID: 48543723
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49fa1bf77a66dbab829aff20ee666ae1a5082cc
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862215"
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
> [!REMARQUE] Une erreur survient lors de l'ajout d'une **colonne** à la collection **Columns** d'un [index](index-object-adox.md) si la **colonne** n'existe pas dans une [table](table-object-adox.md) déjà ajoutée à la collection [Tables](tables-collection-adox.md).


