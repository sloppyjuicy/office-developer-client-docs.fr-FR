---
title: Indexes, collection (ADOX)
TOCTitle: Indexes collection (ADOX)
ms:assetid: ab04bdd1-7c4a-44cb-dfc6-add3a52f502f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249793(v=office.15)
ms:contentKeyID: 48546963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6eac0d1b73e0380f582ce0bc69cdb358c67d185e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291579"
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

