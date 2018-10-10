---
title: Tables, collection (ADOX)
TOCTitle: Tables Collection (ADOX)
ms:assetid: 07bc0541-c528-1c25-c8c4-05736836eda3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248821(v=office.15)
ms:contentKeyID: 48543082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43ca716cf03579c5c4cacf3f6b83a56d549b1433
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470937"
---
# <a name="tables-collection-adox"></a>Tables, collection (ADOX)


**S’applique à**: Access 2013 | Office 2013

Contient tous les objets [Table](table-object-adox.md) d'un catalogue.

## <a name="remarks"></a>Remarques

La méthode [Append](append-method-adox-tables.md) d'une collection **Tables** est unique pour ADOX. Vous pouvez :

  - Ajouter une nouvelle table à la collection à l'aide de la méthode **Append**.

Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :

  - Accéder à une table de la collection à l'aide de la propriété [Item](item-property-ado.md).

  - Renvoyer le nombre de tables de la collection à l'aide de la propriété [Count](count-property-ado.md).

  - Supprimer une table de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).

  - Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l'aide de la méthode [Refresh](refresh-method-ado.md).

Certains fournisseurs peuvent renvoyer d'autres objets de schéma, comme View, dans la collection Tables. Par conséquent, certaines collections ADOX peuvent contenir des références au même objet. En cas de suppression de l'objet d'une collection, la modification apportée ne sera pas visible dans une autre collection qui référence l'objet supprimé tant que vous n'avez pas invoqué la méthode Refresh sur la collection. Par exemple, avec le fournisseur OLE DB Provider for Microsoft Jet, des vues sont renvoyées avec la collection Tables. Si vous en supprimez une, vous devez actualiser la collection Tables pour qu'elle reflète la modification.

