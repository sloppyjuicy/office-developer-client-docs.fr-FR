---
title: Name, propriété (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a65bad49c7b9b7a7af91403b1119923b62daa04a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931245"
---
# <a name="name-property-adox"></a>Name, propriété (ADOX)


**S’applique à**: Access 2013, Office 2013

Indique le nom de l'objet.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String**.

## <a name="remarks"></a>Notes

Les noms ne doivent pas être uniques dans une collection.

La propriété **Name** est en lecture/écriture dans la [colonne](column-object-adox.md), [groupe](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md)et les objets [utilisateur](user-object-adox.md) . La propriété **Name** est en lecture seule sur les objets de [catalogue](catalog-object-adox.md), [Procedure](procedure-object-adox.md)et [View](view-object-adox.md) .

Pour les objets en lecture/écriture (**Column**, **Group**, **Key**, **Index**, **Table** et **User**), la valeur par défaut est une chaîne vide ("").


> [!NOTE]
> <P>[!REMARQUE] Pour les clés, cette propriété est en lecture seule sur les objets <STRONG>Key</STRONG> déjà ajoutés à une collection.</P>




> [!NOTE]
> <P>[!REMARQUE] Pour les tables, elle est en lecture seule sur les objets <STRONG>Table</STRONG> déjà ajoutés à une collection.</P>


