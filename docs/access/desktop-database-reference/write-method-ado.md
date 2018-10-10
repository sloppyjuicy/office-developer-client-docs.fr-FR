---
title: Écrire, méthode - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98af810c9a24d38a6b2b32db31f9a650c2d6f70a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471842"
---
# <a name="write-method-ado"></a>Write, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013


Écrit des données binaires dans un objet [Stream](stream-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Flux de données*. Écrire la*mémoire tampon*

## <a name="parameters"></a>Paramètres

  - *Buffer*

  - Valeur de type **Variant** contenant un tableau d'octets à écrire.

## <a name="remarks"></a>Notes

Les octets spécifiés sont écrits dans l'objet **Stream** sans espaces insérés entre chaque octet.

La propriété [Position](position-property-ado.md) actuelle est définie par l'octet suivant les données écrites. La méthode **Write** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).

Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** augmente pour contenir les nouveaux octets éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.


> [!NOTE]
> <P>La méthode <STRONG>Write</STRONG> est utilisée avec des flux binaires (<A href="type-property-ado-stream.md">Type</A> a la valeur <STRONG>adTypeBinary</STRONG>). Pour les flux de texte (<STRONG>Type</STRONG> a la valeur <STRONG>adTypeText</STRONG>), utilisez la méthode <A href="writetext-method-ado.md">WriteText</A>.</P>


