---
title: SetEOS, méthode (ADO)
TOCTitle: SetEOS method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0856381b288d38c9fc85b5588857477a9c5fa901
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626077"
---
# <a name="seteos-method-ado"></a>SetEOS, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Définit la position qui représente la fin du flux.

## <a name="syntax"></a>Syntaxe

*Stream*. SetEOS

## <a name="remarks"></a>Remarques

**SetEOS** met à jour la valeur de la propriété [EOS](eos-property-ado.md), en définissant la valeur actuelle de la propriété [Position](position-property-ado.md) comme fin du flux. Tous les octets ou caractères qui suivent cette position sont tronqués.

Dans la mesure où les méthodes [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) et [CopyTo](copyto-method-ado.md) ne tronquent aucune valeur supplémentaire dans les objets **Stream** existants, vous pouvez tronquer ces octets ou caractères en définissant la nouvelle position de fin de flux avec **SetEOS**.

> [!WARNING]
> Si vous attribuez à la propriété **EOS** une position qui précède la fin du flux, vous perdrez toutes les données situées après la nouvelle position **EOS**.
