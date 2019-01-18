---
title: MoveFirst, MoveLast, MoveNext et MovePrevious, méthodes (ADO)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (ADO)
ms:assetid: d04ce41c-77c9-df42-115a-65c50a38518a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250039(v=office.15)
ms:contentKeyID: 48547836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2cb6ea7f82ac37460d7f2a4dd998ae7435c04230
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704124"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-ado"></a>MoveFirst, MoveLast, MoveNext et MovePrevious, méthodes (ADO)


**S’applique à**: Access 2013, Office 2013

Accède au premier, au dernier ou à l'enregistrement suivant d'un objet [Recordset](recordset-object-ado.md) spécifié et fait de celui-ci l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="remarks"></a>Notes

Utilisez la méthode **MoveFirst** pour accéder au premier enregistrement de l'objet **Recordset** et faire de celui-ci l'enregistrement actif.

Utilisez la méthode **MoveLast** pour accéder au dernier enregistrement de l'objet **Recordset** et faire de celui-ci l'enregistrement actif. Cet objet **Recordset** doit prendre en charge les signets ou un déplacement du curseur arrière ; sinon, l'appel de la méthode génère une erreur.

Un appel à **MoveFirst** ou **MoveLast** lorsque l'objet **Recordset** est vide (les propriétés **BOF** et **EOF** ont toutes deux la valeur True) génère une erreur.

Utilisez la méthode **MoveNext** pour faire avancer la position de l’enregistrement actif d’un enregistrement (vers la fin de l’objet **Recordset**). Si l’enregistrement actif est le dernier enregistrement et que vous appelez la méthode **MoveNext**, ADO définit l’enregistrement actif à la position qui suit le dernier enregistrement de l’objet **Recordset** (la propriété [EOF](bof-eof-properties-ado.md) a la valeur **True**). Une tentative de déplacement avant lorsque la propriété **EOF** a déjà la valeur **True** génère une erreur.

Dans le cas où l' **objet Recordset** a été filtré ou trié et données de l’enregistrement actif sont modifiées, la position peut également changer. Dans ce cas le **MoveNext** méthode fonctionne normalement, mais vous devez avoir conscience que la position est déplacée d’un enregistrement vers l’avant à partir de la nouvelle position, pas de l’ancien. Par exemple, modification des données dans l’enregistrement en cours, telles que l’enregistrement est déplacé à la fin du **jeu d’enregistrements,** triées signifie que appelant **MoveNext** l'aboutit à ADO la définition de l’enregistrement actif sur la position après le dernier enregistrement dans le ** Jeu d’enregistrements** (**EOF** = **la valeur True**).

Utilisez la méthode **MovePrevious** pour faire reculer la position de l’enregistrement actif d’un enregistrement (vers le début de l’objet **Recordset**). L’objet **Recordset** doit prendre en charge les signets ou le déplacement du curseur arrière ; sinon, la méthod génère une erreur. Si le premier enregistrement est l’enregistrement actif et que vous appelez la méthode **MovePrevious**, ADO définit l’enregistrement actif à la position précédant le premier enregistrement de l’objet **Recordset** (la propriété [BOF](bof-eof-properties-ado.md) a la valeur **True**). Une tentative de déplacement arrière lorsque la propriété **BOF** a déjà la valeur **True** génère une erreur. Si l’objet **Recordset** ne prend pas en charge les signets ou le déplacement du curseur arrière, la méthode **MovePrevious** génère une erreur.

S'il s'agit d'un objet **Recordset** avant uniquement et que vous souhaitez prendre en charge le défilement arrière et avant, vous pouvez utiliser la propriété [CacheSize](cachesize-property-ado.md) pour créer un cache d'enregistrements qui prend en charge le déplacement du curseur arrière via la méthode [Move](move-method-ado.md). Dans la mesure où les enregistrements mis en cache sont chargés en mémoire, évitez de mettre en cache plus d'enregistrements qu'il n'est nécessaire. Vous pouvez appeler la méthode **MoveFirst** dans un objet **Recordset** avant uniquement ; dans un tel cas, il se peut que le fournisseur réexécute la commande qui a généré l'objet **Recordset**.

