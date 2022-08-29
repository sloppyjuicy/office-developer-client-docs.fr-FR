---
title: Write, méthode - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aaf931ca6eb2ded364b7a526ac79946c452a3fac
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365410"
---
# <a name="write-method-ado"></a>Write, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Écrit des données binaires dans un objet [Stream](stream-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Flux*. Écrire *une mémoire tampon*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Buffer* |Valeur de type **Variant** contenant un tableau d'octets à écrire.|

## <a name="remarks"></a>Remarques

Les octets spécifiés sont écrits dans l'objet **Stream** sans espaces insérés entre chaque octet.

La propriété [Position](position-property-ado.md) actuelle est définie par l'octet suivant les données écrites. La méthode **Write** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).

Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de l'objet **Stream** augmente pour contenir les nouveaux octets éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.

> [!NOTE]
> La méthode **Write** est utilisée avec des flux binaires ([Type](type-property-ado-stream.md) a la valeur **adTypeBinary**). Pour les flux de texte (**Type** a la valeur **adTypeText**), utilisez la méthode [WriteText](writetext-method-ado.md).

