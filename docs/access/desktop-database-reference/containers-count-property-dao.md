---
title: Propriété Containers.Count (DAO)
TOCTitle: Count Property
ms:assetid: 3b0bf865-a4d5-82bb-c1a9-9957f110db4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192657(v=office.15)
ms:contentKeyID: 48544276
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7553b0e7d64e059dfeed50f158f21f48455976d7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699946"
---
# <a name="containerscount-property-dao"></a>Propriété Containers.Count (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie le nombre d'objets **[Connection](connection-object-dao.md)** dans la collection **[Connections](connections-collection-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . Nombre

*expression* Variable qui représente un objet **Connections** .

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.

La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.

