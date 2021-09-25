---
title: Ordinal, propriété (Cellule ADO MD)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ba897ff825725eb7ec43d695934bb4840dedee6b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597127"
---
# <a name="ordinal-property-ado-md-cell"></a>Ordinal, propriété (Cellule ADO MD)


**S’applique à** : Access 2013, Office 2013

Identifie de manière unique une cellule au sein d'un ensemble de cellules.

## <a name="return-values"></a>Valeurs de retour

Retourne un entier de type **Long** et est en lecture seule.

## <a name="remarks"></a>Remarques

La valeur ordinale d’une cellule identifie de manière unique la cellule au sein d’un ensemble. En théorie, les cellules sont numérotées dans un ensemble de cellules comme si ce dernier était un tableau *p*-dimensionnel, où *p* correspond au nombre des [axes](axes-collection-ado-md.md). Les cellules sont numérotées à partir de zéro en ordre ligne-majeur.

Utilisée avec la propriété [Item](item-property-ado-md-cellset.md) de l'objet [Cellset](cellset-object-ado-md.md), la valeur ordinale de la cellule permet d'extraire rapidement la [cellule](cell-object-ado-md.md).

