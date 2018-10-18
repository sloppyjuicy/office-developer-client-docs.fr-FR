---
title: DateCreated, propriété (ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f96bdfc7b669aeea279ba746c92bfc299912c70
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602551"
---
# <a name="datecreated-property-adox"></a>DateCreated, propriété (ADOX)


**S’applique à**: Access 2013 | Office 2013

Indique la date de création de l'objet.

<<<<<<< Tête
## <a name="return-values"></a>Valeurs renvoyées
=======
## <a name="return-values"></a>Valeurs de retour
>>>>>>> master

Renvoie une valeur de type **Variant** spécifiant la date de la création. La valeur est Null si la propriété **DateCreated** n'est pas prise en charge par le fournisseur.

## <a name="remarks"></a>Notes

La propriété **DateCreated** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d'obtenir les valeurs de la propriété **DateCreated**.

