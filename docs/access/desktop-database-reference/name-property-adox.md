---
title: Name, propriété (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f067c16c2c7d8d584d6900bff6212b469c3b7fe4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602198"
---
# <a name="name-property-adox"></a>Name, propriété (ADOX)

**S’applique à** : Access 2013, Office 2013

Indique le nom de l'objet.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String**.

## <a name="remarks"></a>Remarques

Les noms ne doivent pas être uniques dans une collection.

The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.

Pour les objets en lecture/écriture (**Column**, **Group**, **Key**, **Index**, **Table** et **User**), la valeur par défaut est une chaîne vide ("").

> [!NOTE]
> - Pour les clés, cette propriété est en lecture seule sur les objets **Key** déjà ajoutés à une collection.
> - [!REMARQUE] Pour les tables, elle est en lecture seule sur les objets **Table** déjà ajoutés à une collection.


