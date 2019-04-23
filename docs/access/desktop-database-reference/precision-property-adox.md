---
title: PreCision, propriété (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f05f6880a9599421189519f263cfb27bf1432325
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287481"
---
# <a name="precision-property-adox"></a>PreCision, propriété (ADOX)


**S’applique à** : Access 2013, Office 2013

Indique la précision maximale de valeurs de données de la colonne.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur de type **Long** qui correspond à la précision maximale des valeurs de données de la colonne lorsque la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) est de type numérique. La propriété **Precision** est ignorée pour tous les autres types de données.

## <a name="remarks"></a>Remarques

La valeur par défaut est zéro (0).

Cette propriété est en lecture seule pour des objets [Column](column-object-adox.md) déjà ajoutés à une collection.

