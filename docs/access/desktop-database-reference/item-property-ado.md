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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718559"
---
# <a name="item-property-ado"></a>Item, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Indique membre spécifique d'une collection, par son nom ou son nombre ordinal.

## <a name="syntax"></a>Syntaxe

Définir*l’objet* = *collection*. Item (Index)

## <a name="return-value"></a>Valeur renvoyée

Renvoie une référence à un objet.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Index* |Une expression **Variant** qui correspond soit au nom, soit au nombre ordinal d'un objet dans une collection.|

## <a name="remarks"></a>Remarques

Utilisez la propriété **Item** pour renvoyer un objet spécifique dans une collection. Si **l’élément** ne peut pas trouver un objet dans la collection correspondant à l’argument *Index* , une erreur se produit. Si la collection ne prend pas en charge les objets nommés, utilisez des nombres ordinaux comme références.

La propriété **Item** est la propriété par défaut de toutes les collections ; les formes de syntaxe suivantes sont donc interchangeables :

```vb
    collection.Item (Index)
    collection (Index)
```
