---
title: Catalog, objet (ADOX)
TOCTitle: Catalog object (ADOX)
ms:assetid: d9e8d94b-9161-3eb6-abaf-00d1244d1f2d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250097(v=office.15)
ms:contentKeyID: 48548068
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d680c89f7188dafd216edf62bd07c80fa924a119
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026238"
---
# <a name="catalog-object-adox"></a>Catalog, objet (ADOX)


**S’applique à**: Access 2013, Office 2013

Contient des collections ([Tables](tables-collection-adox.md), [Views](views-collection-adox.md), [Users](users-collection-adox.md), [Groups](groups-collection-adox.md) et [Procedures](procedures-collection-adox.md)) qui décrivent le catalogue de schémas d'une source de données.

## <a name="remarks"></a>Remarques

Vous pouvez modifier l'objet **Catalog** en ajoutant ou supprimant des objets, ou en modifiant des objets existants. Certains fournisseurs ne prennent pas en charge tous les objets du **catalogue** ou prennent en charge uniquement les informations de schémas d'affichage.

Avec les propriétés et méthodes d'un objet **Catalog**, vous pouvez :

- Ouvrir le catalogue en définissant la propriété [ActiveConnection](activeconnection-property-adox.md) sur un objet [Connection](connection-object-ado.md) ADO ou une chaîne de connexion valide.

- Créer un nouveau catalogue à l'aide de la méthode [Create](create-method-adox.md).

- Identifier les propriétaires des objets dans un **catalogue** à l'aide des méthodes [GetObjectOwner](getobjectowner-method-adox.md) et [SetObjectOwner](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/setobjectowner-method-adox).

