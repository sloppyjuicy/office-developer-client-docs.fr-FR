---
title: ReadText, méthode (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a46a62505f3234dc552db1ed39d38383524cda9e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593802"
---
# <a name="readtext-method-ado"></a>ReadText, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Lit un nombre spécifié de caractères dans un objet [Stream](stream-object-ado.md) de texte.

## <a name="syntax"></a>Syntaxe

*Chaîne*  =  *Stream*. ReadText (*NumChars*)

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*NumChars* |Facultatif. Valeur de type **Long** qui spécifie le nombre de caractères à lire dans le fichier ou une valeur [StreamReadEnum](streamreadenum.md). La valeur par défaut est **adReadAll**.|

## <a name="return-value"></a>Valeur renvoyée

La méthode **ReadText** lit un nombre spécifié de caractères, une ligne complète ou l'intégralité du flux d'un objet **Stream** et retourne la chaîne résultante.

## <a name="remarks"></a>Remarques

Si la valeur de *NbCaractères* est supérieure au nombre de caractères encore présents dans le flux, seuls les caractères restants sont retournés. La chaîne lue n'est pas remplie pour correspondre à la longueur spécifiée par *NbCaractères*. S'il ne reste plus de caractères à lire, une valeur de type Variant NULL est retournée. La méthode **ReadText** ne peut pas être utilisée pour lire à l'envers.

> [!NOTE]
> La méthode **ReadText** est utilisée avec les flux de texte ([Type](type-property-ado-stream.md)**adTypeText**). Pour les flux binaires (**Type****adTypeBinary**), utilisez la méthode [Read](read-method-ado.md).

