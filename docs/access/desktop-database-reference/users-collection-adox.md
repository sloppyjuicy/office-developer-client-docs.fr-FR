---
title: Users, collection (ADOX)
TOCTitle: Users collection (ADOX)
ms:assetid: bc61c862-1637-02e7-4b56-5ad984bdbcb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249905(v=office.15)
ms:contentKeyID: 48547413
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 24d7a5cab3260dac80b39e5134938c5f55175851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312935"
---
# <a name="users-collection-adox"></a>Users, collection (ADOX)

**S’applique à** : Access 2013, Office 2013

Contient tous les objets [User](user-object-adox.md) stockés d’un catalogue ou d’un groupe.

## <a name="remarks"></a>Remarques

La collection **Users** d'un [catalogue](catalog-object-adox.md) représente tous les utilisateurs du catalogue. La collection **Users** d'un [groupe](group-object-adox.md) représente uniquement les utilisateurs appartenant au groupe spécifique.

La méthode [Append](append-method-adox-users.md) d'une collection **Users** est unique pour ADOX. Vous pouvez :

- Ajouter un nouvel utilisateur à la collection à l'aide de la méthode **Append**.

Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :

- Accéder à un utilisateur de la collection à l'aide de la propriété [Item](item-property-ado.md).

- Renvoyer le nombre d'utilisateurs de la collection à l'aide de la propriété [Count](count-property-ado.md).

- Supprimer un utilisateur de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).

- Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l’aide de la méthode [Refresh](refresh-method-ado.md).

> [!NOTE]
> [!REMARQUE] Avant d'ajouter un objet **User** à la collection **Users** d'un objet **Group**, un objet **User** avec le même [nom](name-property-adox.md) que celui à ajouter doit déjà exister dans la collection **Users** du **catalogue**.

