---
title: SetEOS, méthode (ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 420d614d100ed156b794e92f77df2e7a4180c9fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872430"
---
# <a name="seteos-method-ado"></a>SetEOS, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Définit la position qui représente la fin du flux.

## <a name="syntax"></a>Syntaxe

*Flux de données*. SetEOS

## <a name="remarks"></a>Notes

**SetEOS** met à jour la valeur de la propriété [EOS](eos-property-ado.md), en définissant la valeur actuelle de la propriété [Position](position-property-ado.md) comme fin du flux. Tous les octets ou caractères qui suivent cette position sont tronqués.

Dans la mesure où les méthodes [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) et [CopyTo](copyto-method-ado.md) ne tronquent aucune valeur supplémentaire dans les objets **Stream** existants, vous pouvez tronquer ces octets ou caractères en définissant la nouvelle position de fin de flux avec **SetEOS**.


> [!WARNING]
> <P>Si vous attribuez à la propriété <STRONG>EOS</STRONG> une position qui précède la fin du flux, vous perdrez toutes les données situées après la nouvelle position <STRONG>EOS</STRONG>.</P>


