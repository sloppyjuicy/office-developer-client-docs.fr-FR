---
title: Workspaces. Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: bc7c5a11-13d3-27bd-1be4-5d069e888ac2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822719(v=office.15)
ms:contentKeyID: 48547414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 692240130d0a5aa32899b94a18302721da01d44d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302556"
---
# <a name="workspacescount-property-dao"></a>Workspaces. Count, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie le nombre d'objets de la collection spécifiée. En lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Compte

*expression* Variable qui représente un objet **Workspaces** .

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.

Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.

