---
title: SkipLine, méthode (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d22aca01c468813f280472281719822a7d884988
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923923"
---
# <a name="skipline-method-ado"></a>SkipLine, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Saute une ligne complète lors de la lecture d'un flux de texte.

## <a name="syntax"></a>Syntaxe

*Flux de données*. SkipLine

## <a name="remarks"></a>Notes

Tous les caractères, y compris le séparateur de ligne suivante, sont ignorés. Par défaut, [LineSeparator](lineseparator-property-ado.md) prend la valeur **adCRLF**. Si vous tentez de revenir au-delà de [EOS](eos-property-ado.md), la position actuelle reste simplement au niveau de **EOS**.

La méthode **SkipLine** est utilisée avec des flux de texte ([Type](type-property-ado-stream.md) prend la valeur **adTypeText**).

