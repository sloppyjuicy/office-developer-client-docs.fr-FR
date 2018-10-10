---
title: DateModified, propriété (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469419"
---
# <a name="datemodified-property-adox"></a>DateModified, propriété (ADOX)


**S’applique à**: Access 2013 | Office 2013

Indique à la date de la dernière modification de l'objet.

## <a name="return-values"></a>Valeurs de retour

Renvoie une valeur de type **Variant** en spécifiant la date de la modification. La valeur est Null si la propriété **DateModified** n'est pas prise en charge par le fournisseur.

## <a name="remarks"></a>Notes

La propriété **DateModified** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d'obtenir les valeurs de la propriété **DateModified**.

