---
title: DateModified, propriété (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0ed5b0078c934f6aa47422f261b77df248ba4042
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585850"
---
# <a name="datemodified-property-adox"></a>DateModified, propriété (ADOX)


**S’applique à** : Access 2013, Office 2013

Indique à la date de la dernière modification de l'objet.

## <a name="return-values"></a>Valeurs de retour

Renvoie une valeur de type **Variant** en spécifiant la date de la modification. La valeur est Null si la propriété **DateModified** n'est pas prise en charge par le fournisseur.

## <a name="remarks"></a>Remarques

La propriété **DateModified** a la valeur Null pour les objets récemment ajoutés. Après avoir ajouté un nouvel objet [View](view-object-adox.md) ou [Procedure](procedure-object-adox.md), vous devez appeler la méthode [Refresh](refresh-method-ado.md) de la collection [Views](views-collection-adox.md) ou [Procedures](procedures-collection-adox.md) afin d’obtenir les valeurs de la propriété **DateModified**.

