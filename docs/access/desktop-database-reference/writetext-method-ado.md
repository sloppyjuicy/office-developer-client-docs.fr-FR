---
title: WriteText, méthode (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c0c4668141c0da6e5faddee009d2548f1ee2c53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926996"
---
# <a name="writetext-method-ado"></a>WriteText, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Écrit une chaîne de texte spécifiée dans un objet [Stream](stream-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Flux de données*. WriteText les*données*, *Options*

## <a name="parameters"></a>Paramètres

  - *Data*

  - Valeur de type **String** contenant les caractères du texte à écrire.

  - *Options*

  - Facultatif. Valeur [StreamWriteEnum](streamwriteenum.md) spécifiant si un séparateur de ligne doit être écrit à la fin de la chaîne spécifiée.

## <a name="remarks"></a>Notes

Les chaînes spécifiées sont écrites dans l'objet **Stream** sans espace ou caractère inséré entre chaque chaîne.

La propriété [Position](position-property-ado.md) actuelle est définie sur le caractère suivant les données écrites. La méthode **WriteText** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces caractères, appelez [SetEOS](seteos-method-ado.md).

Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** augmente pour contenir les nouveaux caractères éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.


> [!NOTE]
> <P>La méthode <STRONG>WriteText</STRONG> est utilisée avec des flux de texte (<A href="type-property-ado-stream.md">Type</A> a la valeur <STRONG>adTypeText</STRONG>). Pour les flux binaires (<STRONG>Type</STRONG> a la valeur <STRONG>adTypeBinary</STRONG>), utilisez la méthode <A href="write-method-ado.md">Write</A>.</P>


