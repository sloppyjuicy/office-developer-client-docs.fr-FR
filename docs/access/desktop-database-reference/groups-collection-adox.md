---
title: Groups, collection (ADOX)
TOCTitle: Groups collection (ADOX)
ms:assetid: 9aec57df-bc5c-f9b3-5aec-e7e7efa47ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249702(v=office.15)
ms:contentKeyID: 48546553
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b75f6277695c00c251352e0ae2bdcc44f2c86d34
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929152"
---
# <a name="groups-collection-adox"></a>Groups, collection (ADOX)


**S’applique à**: Access 2013, Office 2013

Contient tous les objets [Group](group-object-adox.md) stockés d'un catalogue ou d'un utilisateur.

## <a name="remarks"></a>Remarques

La collection **Groups** d'un [catalogue](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un [utilisateur](user-object-adox.md) représente le groupe auquel l'utilisateur appartient uniquement.

La méthode [Append](append-method-adox-groups.md) d'une collection **Groups** est unique pour ADOX. Vous pouvez :

  - Ajouter un nouveau groupe de sécurité à la collection à l'aide de la méthode **Append**.

Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :

  - Accéder à un groupe de la collection à l'aide de la propriété [Item](item-property-ado.md).

  - Renvoyer le nombre de groupes de la collection à l'aide de la propriété [Count](count-property-ado.md).

  - Supprimer un groupe de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).

  - Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).


> [!NOTE]
> <P>[!REMARQUE] Avant d'ajouter un objet <STRONG>Group</STRONG> à la collection <STRONG>Groups</STRONG> d'un objet <STRONG>User</STRONG>, un objet <STRONG>Group</STRONG> avec le même <A href="name-property-adox.md">nom</A> que celui à ajouter doit déjà exister dans la collection <STRONG>Groups</STRONG> du <STRONG>catalogue</STRONG>.</P>


