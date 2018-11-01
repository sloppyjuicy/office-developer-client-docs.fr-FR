---
title: Table, objet (ADOX)
TOCTitle: Table Object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b63014a57104d5d31f5ac5620b26712a9f97347b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869293"
---
# <a name="table-object-adox"></a>Table, objet (ADOX)


**S’applique à**: Access 2013, Office 2013

Représente une table de base de données comprenant des colonnes, des index et des clés.

## <a name="remarks"></a>Remarques

Le code suivant permet de créer une nouvelle **table**:

`Dim obj As New Table`

Avec les propriétés et collections d'un objet **Table**, vous pouvez :

  - Identifier la table à l'aide de la propriété [Name](name-property-adox.md).

  - Déterminer le type de la table à l'aide de la propriété [Type](https://msdn.microsoft.com/library/jj250042\(v=office.15\)).

  - Accéder aux colonnes de base de données de la table à l'aide de la collection [Columns](columns-collection-adox.md).

  - Accéder aux index de la table à l'aide de la collection [Indexes](indexes-collection-adox.md).

  - Accéder aux clés de la table à l'aide de la collection [Keys](keys-collection-adox.md).

  - Spécifier le [catalogue](catalog-object-adox.md) auquel appartient la table à l'aide de la propriété [ParentCatalog](parentcatalog-property-adox.md).

  - Renvoyer des informations de date à l'aide des propriétés [DateCreated](datecreated-property-adox.md) et [DateModified](datemodified-property-adox.md).

  - Accéder aux propriétés de table spécifiques au fournisseur à l'aide de la collection [Properties](properties-collection-ado.md).


> [!NOTE]
> <P>[!REMARQUE] Votre fournisseur de données peut ne pas prendre en charge toutes les propriétés de l'objet <STRONG>Table</STRONG>. Une erreur survient si vous avez défini une valeur pour une propriété non prise en charge par le fournisseur. Pour les nouveaux objets <STRONG>Table</STRONG>, l'erreur survient lorsque l'objet est ajouté à la collection. Pour les objets existants, elle survient au moment de la définition de la propriété.</P>



Lors de la création des objets **Table**, l'existence d'une valeur par défaut appropriée pour une propriété facultative ne garantit pas que votre fournisseur prend en charge la propriété. Pour plus d'informations sur les propriétés prises en charge par votre fournisseur, reportez-vous à sa documentation.

