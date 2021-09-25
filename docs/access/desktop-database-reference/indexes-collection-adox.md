---
title: Indexes, collection (ADOX)
TOCTitle: Indexes collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 007d6803138a02bdfac5da55abbc3c990404dad3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602373"
---
# <a name="indexes-collection-adox"></a>Indexes, collection (ADOX)


**S’applique à** : Access 2013, Office 2013

Contient tous les objets [Index](index-object-adox.md) d’une table.

## <a name="remarks"></a>Remarques

La méthode [Append](append-method-adox-indexes.md) d'une collection **Indexes** est unique pour ADOX. Vous pouvez :

  - Ajouter un nouvel index à la collection à l'aide de la méthode **Append**.

Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :

  - Accéder à un index de la collection à l'aide de la propriété [Item](item-property-ado.md).

  - Renvoyer le nombre d'index de la collection à l'aide de la propriété [Count](count-property-ado.md).

  - Supprimer un index de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).

  - Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l’aide de la méthode [Refresh](refresh-method-ado.md).

