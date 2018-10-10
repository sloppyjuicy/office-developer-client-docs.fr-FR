---
title: Item, propriété (ADO)
TOCTitle: Item Property (ADO)
ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15)
ms:contentKeyID: 48545767
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29453ac2801f606640fd6d9506a8ee1ee8625396
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469361"
---
# <a name="item-property-ado"></a>Item, propriété (ADO)

**S’applique à**: Access 2013 | Office 2013

Indique membre spécifique d'une collection, par son nom ou son nombre ordinal.

## <a name="syntax"></a>Syntaxe

Définir*l’objet* = *collection*. Item (Index)

## <a name="return-value"></a>Valeur renvoyée

Renvoie une référence à un objet.

## <a name="parameters"></a>Paramètres

- *Index*

- Une expression **Variant** qui correspond soit au nom, soit au nombre ordinal d'un objet dans une collection.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Item** pour renvoyer un objet spécifique dans une collection. Si **l’élément** ne peut pas trouver un objet dans la collection correspondant à l’argument *Index* , une erreur se produit. Si la collection ne prend pas en charge les objets nommés, utilisez des nombres ordinaux comme références.

La propriété **Item** est la propriété par défaut de toutes les collections ; les formes de syntaxe suivantes sont donc interchangeables :

```vb
    collection.Item (Index)
    collection (Index)
```
