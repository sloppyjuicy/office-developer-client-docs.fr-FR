---
title: Keys, collection (ADOX)
TOCTitle: Keys collection (ADOX)
ms:assetid: 0d480c01-1b36-28b9-9135-51958f313995
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248854(v=office.15)
ms:contentKeyID: 48543215
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 82718af6378b13c4b0350dca84a84f06afd682de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626343"
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

