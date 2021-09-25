---
title: LineSeparator, propriété (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 447acfe8c498975b41ce007f8abd669ade8ee6a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602338"
---
# <a name="lineseparator-property-ado"></a>LineSeparator, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le caractère binaire à utiliser comme le séparateur de ligne dans des objets [Stream](stream-object-ado.md) textuels.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur [LineSeparatorsEnum](lineseparatorsenum.md) qui indique le caractère séparateur de ligne utilisé dans le **Stream**. La valeur par défaut est **adCRLF**.

## <a name="remarks"></a>Remarques

**LineSeparator** sert à interpréter les lignes à la lecture du contenu d’un **Stream** textuel. Les lignes peuvent être ignorées grâce à la méthode [SkipLine](skipline-method-ado.md).

**LineSeparator** n’est utilisé qu’avec les objets **Stream** textuels (dont le [Type](type-property-ado-stream.md) est **adTypeText**). Cette propriété est ignorée si le **Type** est **adTypeBinary**.

