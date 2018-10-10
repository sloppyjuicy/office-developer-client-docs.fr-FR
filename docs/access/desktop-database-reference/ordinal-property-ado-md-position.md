---
title: Ordinal, propriété (objet Position ADO MD)
TOCTitle: Ordinal Property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e953c038947073d3cdeb971e705c80f63d12a15b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469737"
---
# <a name="ordinal-property-ado-md-position"></a>Ordinal, propriété (objet Position ADO MD)


**S’applique à**: Access 2013 | Office 2013

Identifie de façon unique une position le long d'un axe.

## <a name="return-values"></a>Valeurs de retour

Renvoie un nombre entier de type **Long** et est en lecture seule.

## <a name="remarks"></a>Notes

L' **Ordinal** d’un objet [Position](position-object-ado-md.md) correspond à l’index de la **Position** dans la collection [Positions](positions-collection-ado-md.md) .

Il est possible de récupérer rapidement une cellule en utilisant la propriété **Ordinal** de l'objet **Position** le long de chaque axe avec la propriété [Item](item-property-ado-md-cellset.md) de l'objet [Cellset](cellset-object-ado-md.md).

