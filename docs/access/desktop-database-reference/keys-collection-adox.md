---
title: Keys, collection (ADOX)
TOCTitle: Keys collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f43e6643e585ed8c28cd710e0674523b84d12d89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290249"
---
# <a name="keys-collection-adox"></a>Keys, collection (ADOX)


**S’applique à** : Access 2013, Office 2013

Contient tous les objets [Key](key-object-adox.md) d’une table.

## <a name="remarks"></a>Remarques

La méthode [Append](append-method-adox-keys.md) d'une collection **Key** est unique pour ADOX. Vous pouvez :

  - Ajouter une nouvelle clé à la collection à l'aide de la méthode **Append**.

Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :

  - Accéder à une clé de la collection à l'aide de la propriété [Item](item-property-ado.md).

  - Renvoyer le nombre de clés de la collection à l'aide de la propriété [Count](count-property-ado.md).

  - Supprimer une clé de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).

  - Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l’aide de la méthode [Refresh](refresh-method-ado.md).

