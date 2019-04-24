---
title: Item, propriété (ADO)
TOCTitle: Item property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cc38101cb17c52bf2c8c08c08c14163c3772b2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290792"
---
# <a name="item-property-ado"></a>Item, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Indique membre spécifique d'une collection, par son nom ou son nombre ordinal.

## <a name="syntax"></a>Syntaxe

Définir la*collection*d'*objets* = . Item (index)

## <a name="return-value"></a>Valeur renvoyée

Renvoie une référence à un objet.

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*Index* |Une expression **Variant** qui correspond soit au nom, soit au nombre ordinal d'un objet dans une collection.|

## <a name="remarks"></a>Remarques

Utilisez la propriété **Item** pour renvoyer un objet spécifique dans une collection. Si **Item** ne parvient pas à trouver un objet dans la collection correspondant à l'argument *Index*, une erreur est générée. Si la collection ne prend pas en charge les objets nommés, utilisez des nombres ordinaux comme références.

La propriété **Item** est la propriété par défaut de toutes les collections ; par conséquent, les formes syntaxiques suivantes sont interchangeables :

```vb
    collection.Item (Index)
    collection (Index)
```
