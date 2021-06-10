---
title: CopyTo, méthode (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295477"
---
# <a name="copyto-method-ado"></a>CopyTo, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Copie le nombre de caractères ou d’octets spécifié (selon la propriété [Type](type-property-ado-stream.md)) d’un objet [Stream](stream-object-ado.md) vers un autre objet **Stream**.

## <a name="syntax"></a>Syntaxe

*Stream*. CopyTo *DestStream*, *NumChars*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*DestStream* |Valeur de variable objet contenant une référence à un objet **Stream** ouvert. L'objet **Stream** actif est copié dans l'objet **Stream** de destination spécifié par *DestStream*. L'objet **Stream** de destination doit être déjà ouvert sans quoi une erreur d'exécution est générée.

<br/><br/>**REMARQUE**: le *paramètre DestStream* peut ne pas être un proxy de l’objet **Stream,** car cela nécessite l’accès à une interface privée sur l’objet **Stream** qui ne peut pas être distante vers le client.|
|*NumChars* |Facultatif. Valeur de type **Integer** qui spécifie le nombre d’octets ou de caractères à copier de la position actuelle dans l’objet **Stream** source vers l’objet **Stream** de destination. La valeur par défaut est –1, ce qui signifie que tous les caractères ou tous les octets sont copiés de la position actuelle vers [EOS](eos-property-ado.md).|

## <a name="remarks"></a>Remarques

Cette méthode copie le nombre spécifié de caractères ou d’octets à partir de la position actuelle spécifiée par la propriété [Position](position-property-ado.md). Si le nombre spécifié est supérieur au nombre d’octets disponibles jusqu’à **EOS**, seuls les caractères ou les octets de la position actuelle jusqu’à **EOS** sont copiés. Si *NumChars* a la valeur –1 ou est omis, tous les caractères ou octets sont copiés à partir de la position actuelle.

Si le flux de destination contient déjà des caractères ou des octets, tout le contenu au-delà du point où se termine la copie est conservé et n'est pas tronqué. **Position** devient l'octet suivant immédiatement le dernier octet copié. Si vous voulez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).

Utilisez **CopyTo** pour copier des données dans un objet **Stream** de destination du même type que l’objet **Stream** source (les paramètres de la propriété **Type** de ces deux objets doivent avoir tous deux la valeur **adTypeText** ou **adTypeBinary**). Pour des objets **Stream** de texte, vous pouvez modifier le paramètre de la propriété [Charset](charset-property-ado.md) de l’objet **Stream** de destination afin de pouvoir changer le jeu de caractères. Par ailleurs, vous pouvez copier des objets **Stream** de texte dans des objets **Stream** binaires, mais pas des objets **Stream** binaires dans des objets **Stream** de texte.

