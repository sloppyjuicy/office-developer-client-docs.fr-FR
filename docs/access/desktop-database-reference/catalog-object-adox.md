---
title: Objet Catalog (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e27cd70863288c2e68020f70149f6d62c75b5662
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66083568"
---
# <a name="catalog-object-adox"></a>Objet Catalog (ADOX)


**S’applique à** : Access 2013, Office 2013

Contient des collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) et [Procedures](procedures-collection-adox.md)) qui décrivent le catalogue de schémas d’une source de données.

## <a name="remarks"></a>Remarques

Vous pouvez modifier l'objet **Catalog** en ajoutant ou supprimant des objets, ou en modifiant des objets existants. Certains fournisseurs ne prennent pas en charge tous les objets du **catalogue** ou prennent en charge uniquement les informations de schémas d'affichage.

Avec les propriétés et méthodes d'un objet **Catalog**, vous pouvez :

- Ouvrir le catalogue en définissant la propriété [ActiveConnection](activeconnection-property-adox.md) sur un objet [Connection](connection-object-ado.md) ADO ou une chaîne de connexion valide.

- Créer un nouveau catalogue à l’aide de la méthode [Create](create-method-adox.md).

- Identifier les propriétaires des objets dans un **catalogue** à l’aide des méthodes [GetObjectOwner](getobjectowner-method-adox.md) et [SetObjectOwner](/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox).
