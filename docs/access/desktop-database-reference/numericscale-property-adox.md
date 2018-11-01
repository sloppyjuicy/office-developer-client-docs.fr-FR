---
title: NumericScale, propriété (ADOX)
TOCTitle: NumericScale Property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 11696e379fe618f07a6087eee26ba21a2d27b3e5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890917"
---
# <a name="numericscale-property-adox"></a>NumericScale, propriété (ADOX)


**S’applique à**: Access 2013, Office 2013

Indique l'échelle d'une valeur numérique de la colonne.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur de type **Byte** qui correspond à l'échelle des valeurs de données de la colonne lorsque la propriété [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) a pour valeur **adNumeric** ou **adDecimal**. **NumericScale** est ignoré pour tous les autres types de données.

## <a name="remarks"></a>Notes

La valeur par défaut est zéro (0).

**NumericScale** est en lecture seule pour les objets [Column](column-object-adox.md) déjà ajoutés à une collection.

