---
title: Documents.Count Property (DAO)
TOCTitle: Count Property
ms:assetid: 3fc0b1e6-f7be-cd43-711f-5cf5763fe7f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192858(v=office.15)
ms:contentKeyID: 48544407
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053325
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab406b0d8141b0b7c1b22956bc1eb58906361915
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870610"
---
# <a name="documentscount-property-dao"></a>Documents.Count Property (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie le nombre d'objets dans la collection spécifiée. En lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Nombre

*expression* Variable qui représente un objet **Documents** .

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.

La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.

