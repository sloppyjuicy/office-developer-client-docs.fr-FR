---
title: Views, collection (ADOX)
TOCTitle: Views collection (ADOX)
ms:assetid: 8d0f9517-4be1-be9c-d4cd-6d50cd5a8983
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249618(v=office.15)
ms:contentKeyID: 48546246
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1eec2b99fabcd0b23970ebaa9c17103ea512c0ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572605"
---
# <a name="views-collection-adox"></a>Views, collection (ADOX)


**S’applique à** : Access 2013, Office 2013

Contient tous les objets [View](view-object-adox.md) d’un catalogue.

## <a name="remarks"></a>Remarques

La méthode [Append](append-method-adox-views.md) d'une collection **Views** est unique pour ADOX. Vous pouvez :

  - Ajouter une nouvelle vue à la collection à l'aide de la méthode **Append**.

Les propriétés et méthodes restantes sont des collections ADO standard. Vous pouvez :

  - Accéder à une vue de la collection à l'aide de la propriété [Item](item-property-ado.md).

  - Renvoyer le nombre de vues de la collection à l'aide de la propriété [Count](count-property-ado.md).

  - Supprimer une vue de la collection à l'aide de la méthode [Delete](delete-method-adox-collections.md).

  - Mettre à jour les objets de la collection afin de refléter le schéma de la base de données active à l’aide de la méthode [Refresh](refresh-method-ado.md).

