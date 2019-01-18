---
title: Propriété Errors.Count (DAO)
TOCTitle: Count Property
ms:assetid: ad135955-3b18-4f99-66d9-aff1492df13b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821719(v=office.15)
ms:contentKeyID: 48547028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2cbbed2c7061b225d969dbd7554191e8db4a28a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707254"
---
# <a name="errorscount-property-dao"></a>Propriété Errors.Count (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie le nombre d'objets dans la collection spécifiée. En lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Nombre

*expression* Variable qui représente un objet **Errors** .

## <a name="remarks"></a>Remarques

Étant donné que les membres d'une collection commencent par 0, vous avez toujours intérêt à coder les boucles en commençant par le membre 0 et en finissant par la valeur de la propriété **Count** moins 1. Si vous voulez effectuer une boucle sur tous les membres d'une collection sans vérifier la propriété **Count**, vous pouvez utiliser la commande **For Each...Next**.

La valeur de la propriété **Count** n'est jamais Null. Si sa valeur est égale à 0, cela signifie qu'il n'y a pas d'objet dans la collection.

