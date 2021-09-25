---
title: Read, méthode - ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2588df93b014d4e5ca85b0b545b0a18bfa751174
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593809"
---
# <a name="read-method-ado"></a>Read, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Lit un nombre spécifié d’octets dans un objet [Stream](stream-object-ado.md) binaire.

## <a name="syntax"></a>Syntaxe

*Variant*  =  *Stream*. Read (*NumBytes* )

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*NumBytes* |Facultatif. Valeur de type **Long** qui spécifie le nombre d'octets à lire dans le fichier ou la valeur [StreamReadEnum](streamreadenum.md) **adReadAll**, qui constitue la valeur par défaut.|

## <a name="return-value"></a>Valeur renvoyée

La méthode **Read** lit un nombre spécifié d'octets ou l'intégralité du flux d'un objet **Stream** et retourne les données résultantes sous la forme de données de type **Variant**.

## <a name="remarks"></a>Remarques

Si la valeur de *NbOctets* est supérieure au nombre d'octets laissés dans l'objet **Stream**, seuls les octets restants sont retournés. Les données lues ne sont pas remplies afin de correspondre à la longueur spécifiée par *NbOctets*. S'il ne reste plus d'octet à lire, une valeur de type Variant NULL est retournée. La méthode **Read** ne peut pas être utilisée pour lire à l'envers.

> [!NOTE]
> *NbOctets* mesure toujours des octets. Pour les objets **Stream** contenant du texte ([Type](type-property-ado-stream.md)**adTypeText**), utilisez [ReadText](readtext-method-ado.md).


