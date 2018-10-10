---
title: Read, méthode - ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fcc4c3039e1e55bb6bd33078542faa880d27ded
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470254"
---
# <a name="read-method-ado"></a>Read, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013

Lit un nombre spécifié d'octets dans un objet [Stream](stream-object-ado.md) binaire.

## <a name="syntax"></a>Syntaxe

*Variant* = *flux*. Lecture (*NbOctets* )

## <a name="parameters"></a>Paramètres

  - *Valeur du paramètre NbOctets*

  - Facultatif. Valeur de type **Long** qui spécifie le nombre d'octets à lire dans le fichier ou la valeur [StreamReadEnum ](streamreadenum.md) **adReadAll**, qui constitue la valeur par défaut.

## <a name="return-value"></a>Valeur de retour

La méthode **Read** lit un nombre spécifié d'octets ou l'intégralité du flux d'un objet **Stream** et retourne les données résultantes sous la forme de données de type **Variant**.

## <a name="remarks"></a>Notes

Si la valeur de *NbOctets* est supérieure au nombre d'octets laissés dans l'objet **Stream**, seuls les octets restants sont retournés. Les données lues ne sont pas remplies afin de correspondre à la longueur spécifiée par *NbOctets*. S'il ne reste plus d'octet à lire, une valeur de type Variant NULL est retournée. La méthode **Read** ne peut pas être utilisée pour lire à l'envers.


> [!NOTE]
> <P><EM>NbOctets</EM> mesure toujours des octets. Pour les objets <STRONG>Stream</STRONG> contenant du texte (<A href="type-property-ado-stream.md">Type </A><STRONG>adTypeText</STRONG>), utilisez <A href="readtext-method-ado.md">ReadText</A>.</P>


