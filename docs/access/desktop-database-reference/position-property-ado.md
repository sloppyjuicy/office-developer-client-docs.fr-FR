---
title: Position, propriété (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dca9eac0014b6c80a498f70474c2715e1c17959c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562474"
---
# <a name="position-property-ado"></a>Position, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Indique la position actuelle dans un objet [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou retourne une valeur de type **Long** qui spécifie le décalage, en nombre d'octets, de la position actuelle par rapport au début du flux. La valeur par défaut est 0 ; elle représente le premier octet du flux.

## <a name="remarks"></a>Remarques

La position actuelle peut être définie au-delà de la fin du flux. Dans ce cas, la propriété [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de l'objet **Stream** est augmentée en conséquence. Les nouveaux octets ajoutés de cette façon sont nuls.

> [!NOTE]
> [!REMARQUE] **Position** mesure toujours des octets. Pour les flux de texte utilisant des jeux de caractères multioctet, multipliez la position par la taille de caractères pour déterminer le numéro du caractère. Par exemple, dans un jeu de caractères de deux octets, le premier caractère est en position 0, le deuxième en position 2, le troisième en position 4, etc.

Il est impossible d'utiliser des valeurs négatives pour modifier la position actuelle dans un **Stream**. La propriété **Position** n'accepte que les chiffres positifs.

For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**. This does not change the size of the **Stream**, or alter the **Stream** contents in any way. However, doing this should be avoided because it results in a meaningless **Position** value.

