---
title: ReadText, méthode (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4bc9febb76f71068517d2d83cddbdf4edee53b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891134"
---
# <a name="readtext-method-ado"></a>ReadText, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Lit un nombre spécifié de caractères dans un objet [Stream](stream-object-ado.md) de texte.

## <a name="syntax"></a>Syntaxe

*Chaîne* = *flux*. ReadText (*NumChars*)

## <a name="parameters"></a>Paramètres

  - *NumChars*

  - Facultatif. Valeur de type **Long** qui spécifie le nombre de caractères à lire dans le fichier ou une valeur [StreamReadEnum](streamreadenum.md). La valeur par défaut est **adReadAll**.

## <a name="return-value"></a>Valeur renvoyée

La méthode **ReadText** lit un nombre spécifié de caractères, une ligne complète ou l'intégralité du flux d'un objet **Stream** et retourne la chaîne résultante.

## <a name="remarks"></a>Notes

Si la valeur de *NbCaractères* est supérieure au nombre de caractères encore présents dans le flux, seuls les caractères restants sont retournés. La chaîne lue n'est pas remplie pour correspondre à la longueur spécifiée par *NbCaractères*. S'il ne reste plus de caractères à lire, une valeur de type Variant NULL est retournée. La méthode **ReadText** ne peut pas être utilisée pour lire à l'envers.


> [!NOTE]
> <P>La méthode <STRONG>ReadText</STRONG> est utilisée avec les flux de texte (<A href="type-property-ado-stream.md">Type </A><STRONG>adTypeText</STRONG>). Pour les flux binaires (<STRONG>Type </STRONG><STRONG>adTypeBinary</STRONG>), utilisez la méthode <A href="read-method-ado.md">Read</A>.</P>


