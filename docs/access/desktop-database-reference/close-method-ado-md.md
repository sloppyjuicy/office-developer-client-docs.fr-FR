---
title: Close, méthode (ADO MD)
TOCTitle: Close method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 609069d04124146f311166e3ae56d8d6a793675b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296317"
---
# <a name="close-method-ado-md"></a>Close, méthode (ADO MD)


**S’applique à** : Access 2013, Office 2013

Ferme un ensemble de cellules ouvert.

## <a name="syntax"></a>Syntaxe

*Cellset*. Fermer

## <a name="remarks"></a>Remarques

Lorsque vous fermez un objet [Cellset](cellset-object-ado-md.md) à l’aide de la méthode **Close**, vous libérez les données associées, ainsi que celles de tous les objets [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md) ou [Member](member-object-ado-md.md) liés. La fermeture d’un objet **Cellset** n’engendre pas sa suppression de la mémoire. Vous pourrez modifier les paramètres de ses propriétés et le rouvrir ultérieurement. Pour supprimer définitivement un objet de la mémoire, affectez à la variable objet la valeur **Nothing**.

Par la suite, vous pourrez appeler la méthode [Open](open-method-ado-md.md) pour rouvrir l'objet **Cellset** à l'aide de la même chaîne source ou d'une autre. Lorsque l'objet **Cellset** est fermé, une erreur se produit si vous tentez d'extraire une propriété ou d'appeler une méthode qui fait référence aux données ou métadonnées sous-jacentes.

