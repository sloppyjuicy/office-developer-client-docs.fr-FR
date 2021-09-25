---
title: Count, propriété (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c31bd1d3c811fdb0faa8036e247c4aafe5223409
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586032"
---
# <a name="count-property-ado"></a>Count, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le nombre d'objets d'une collection.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long**

## <a name="remarks"></a>Remarques

Utilisez la propriété **Count** pour déterminer le nombre d'objets figurant dans une collection déterminée.

Dans la mesure où la numérotation des membres d'une collection commence par 0, vous devez toujours coder les boucles en commençant par le membre 0 et finir par la valeur de la propriété **Count** moins 1. Si vous utilisez Microsoft Visual Basic et que vous souhaitez parcourir les membres d'une collection sans vérifier la propriété **Count**, utilisez la commande **For** **Each...Next**.

Si la propriété **Count** a la valeur 0, il n'y a pas d'objets dans la collection.

