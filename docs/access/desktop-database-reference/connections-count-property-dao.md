---
title: Connections.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 9b2f0aaa-785a-7fe7-15c3-aea37fdacd12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198023(v=office.15)
ms:contentKeyID: 48546563
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c4f341abfea455acdc96a2883d0f4dee3bd2a5fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469826"
---
# <a name="connectionscount-property-dao"></a>Connections.Count Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Renvoie le nombre d'objets **[Connection](connection-object-dao.md)** dans la collection **[Connections](connections-collection-dao.md)**.

## <a name="syntax"></a>Syntaxe

*expression* . Nombre

*expression* Variable qui représente un objet **Connections** .

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.

La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.

