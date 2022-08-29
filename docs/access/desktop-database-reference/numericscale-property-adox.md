---
title: NumericScale, propriété (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d91d28414cf3ad30d96b38ea2ae3d7340c7388bf
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365851"
---
# <a name="numericscale-property-adox"></a>NumericScale, propriété (ADOX)


**S’applique à** : Access 2013, Office 2013

Indique l'échelle d'une valeur numérique de la colonne.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit et renvoie une valeur de type **Byte** qui correspond à l’échelle des valeurs de données de la colonne lorsque la propriété [Type](/office/vba/access/concepts/miscellaneous/type-property-columnadox) a pour valeur **adNumeric** ou **adDecimal**. **NumericScale** est ignoré pour tous les autres types de données.

## <a name="remarks"></a>Remarques

La valeur par défaut est zéro (0).

**NumericScale** est en lecture seule pour les objets [Column](column-object-adox.md) déjà ajoutés à une collection.

