---
title: WriteText, méthode (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f2a65373add9263bac97ca20a9f29de4307599f
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025839"
---
# <a name="writetext-method-ado"></a>WriteText, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Écrit une chaîne de texte spécifiée dans un objet [Stream](stream-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Flux de données*. WriteText les*données*, *Options*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Data* |Valeur de type **String** contenant les caractères du texte à écrire.|
|*Options* |Facultatif. Valeur [StreamWriteEnum](streamwriteenum.md) spécifiant si un séparateur de ligne doit être écrit à la fin de la chaîne spécifiée.|

## <a name="remarks"></a>Notes

Les chaînes spécifiées sont écrites dans l'objet **Stream** sans espace ou caractère inséré entre chaque chaîne.

La propriété [Position](position-property-ado.md) actuelle est définie sur le caractère suivant les données écrites. La méthode **WriteText** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces caractères, appelez [SetEOS](seteos-method-ado.md).

Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de l'objet **Stream** augmente pour contenir les nouveaux caractères éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.

> [!NOTE]
> La méthode **WriteText** est utilisée avec des flux de texte ([Type](type-property-ado-stream.md) a la valeur **adTypeText**). Pour les flux binaires (**Type** a la valeur **adTypeBinary**), utilisez la méthode [Write](write-method-ado.md).


