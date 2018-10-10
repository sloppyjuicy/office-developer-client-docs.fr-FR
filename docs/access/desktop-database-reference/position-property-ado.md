---
title: Position, propriété (ADO)
TOCTitle: Position Property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a06810fe339bd9b0b24137e178517c062962c096
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470610"
---
# <a name="position-property-ado"></a>Position, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique la position actuelle dans un objet [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs renvoyées

Définit ou retourne une valeur de type **Long** qui spécifie le décalage, en nombre d'octets, de la position actuelle par rapport au début du flux. La valeur par défaut est 0 ; elle représente le premier octet du flux.

## <a name="remarks"></a>Remarques

La position actuelle peut être définie au-delà de la fin du flux. Dans ce cas, la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** est augmentée en conséquence. Les nouveaux octets ajoutés de cette façon sont nuls.


> [!NOTE]
> <P>[!REMARQUE] <STRONG>Position</STRONG> mesure toujours des octets. Pour les flux de texte utilisant des jeux de caractères multioctet, multipliez la position par la taille de caractères pour déterminer le numéro du caractère. Par exemple, dans un jeu de caractères de deux octets, le premier caractère est en position 0, le deuxième en position 2, le troisième en position 4, etc.</P>



Il est impossible d'utiliser des valeurs négatives pour modifier la position actuelle dans un **Stream**. La propriété **Position** n'accepte que les chiffres positifs.

Pour les objets **Stream** en lecture seule, ADO ne renvoie pas une erreur si la **Position** est définie sur une valeur supérieure à la **taille** du **flux de données**. Cela ne pas modifier la taille du **flux**ou **son contenu** . Toutefois, cette opération doit être évitée, car elle génère une valeur de **Position** sans signification.

