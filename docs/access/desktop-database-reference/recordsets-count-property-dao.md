---
title: Recordsets.Count, propriété (DAO)
TOCTitle: Count Property
ms:assetid: 4362aa16-c8e9-e517-887e-c4532bd1eef9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192940(v=office.15)
ms:contentKeyID: 48544500
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b39983dcfd0399667c7b19bb67c3fc64c7eac7ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589168"
---
# <a name="recordsetscount-property-dao"></a>Recordsets.Count, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie le nombre d'objets dans la collection spécifiée. Valeur **Integer** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* Count

*expression* Variable qui représente un objet **Recordsets.**

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous devez toujours coder les boucles en commençant par le membre 0 et en terminant par la valeur de la propriété **Count** moins 1. Si vous souhaitez effectuer une boucle sur les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser un **For Each... Prochain** commande.

Le paramètre de la propriété **Count** n'est jamais Null. Si sa valeur est 0, il n'y a pas d'objets dans la collection.

