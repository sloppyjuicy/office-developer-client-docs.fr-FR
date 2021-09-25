---
title: Workspaces.Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: bc7c5a11-13d3-27bd-1be4-5d069e888ac2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822719(v=office.15)
ms:contentKeyID: 48547414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 485c43b6cc345777d9567b62e984fed4d4bfe482
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588538"
---
# <a name="workspacescount-property-dao"></a>Workspaces.Count, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie le nombre d'objets de la collection spécifiée. En lecture seule.

## <a name="syntax"></a>Syntaxe

*.* Count

*expression* Variable qui représente un **objet Workspaces.**

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.

Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.

