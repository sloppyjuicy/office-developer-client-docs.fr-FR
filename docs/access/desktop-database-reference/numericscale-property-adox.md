---
title: NumericScale, propriété (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b1a15f78463ca0ff6e690b600b9cdca7cc194c7
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025958"
---
# <a name="numericscale-property-adox"></a>NumericScale, propriété (ADOX)


**S’applique à**: Access 2013, Office 2013

Indique l'échelle d'une valeur numérique de la colonne.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur de type **Byte** qui correspond à l'échelle des valeurs de données de la colonne lorsque la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) a pour valeur **adNumeric** ou **adDecimal**. **NumericScale** est ignoré pour tous les autres types de données.

## <a name="remarks"></a>Notes

La valeur par défaut est zéro (0).

**NumericScale** est en lecture seule pour les objets [Column](column-object-adox.md) déjà ajoutés à une collection.

