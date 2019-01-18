---
title: LineSeparator, propriété (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720673"
---
# <a name="lineseparator-property-ado"></a>LineSeparator, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique le caractère binaire à utiliser comme le séparateur de ligne dans des objets [Stream](stream-object-ado.md) textuels.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur [LineSeparatorsEnum](lineseparatorsenum.md) qui indique le caractère séparateur de ligne utilisé dans le **Stream**. La valeur par défaut est **adCRLF**.

## <a name="remarks"></a>Remarques

**LineSeparator** sert à interpréter les lignes à la lecture du contenu d'un **Stream** textuel. Les lignes peuvent être ignorées grâce à la méthode [SkipLine](skipline-method-ado.md).

**LineSeparator** n’est utilisé qu’avec les objets **Stream** textuels (dont le [Type](type-property-ado-stream.md) est **adTypeText**). Cette propriété est ignorée si le **Type** est **adTypeBinary**.

