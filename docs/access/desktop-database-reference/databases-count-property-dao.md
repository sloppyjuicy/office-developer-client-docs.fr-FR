---
title: Databases.Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: 7c542b17-9806-e00e-8cbd-58d6d17e98c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196364(v=office.15)
ms:contentKeyID: 48545831
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 02afe712b1db6ccbd0f959ebbc03ccac29296c6d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565582"
---
# <a name="databasescount-property-dao"></a>Databases.Count, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie le nombre d'objets de la collection spécifiée. En lecture seule.

## <a name="syntax"></a>Syntaxe

*.* Count

*expression* Variable qui représente un objet **Databases.**

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.

Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.

