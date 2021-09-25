---
title: Identification des éléments pris en charge
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 360a9e7a1f7dff51093216d0658cf72d74855b03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553094"
---
# <a name="determining-what-is-supported"></a>Identification des éléments pris en charge

**S’applique à** : Access 2013, Office 2013

La méthode **Supports** permet de déterminer si un objet **Recordset** spécifié prend en charge un type donné de fonctionnalité. Sa syntaxe est la suivante :

`boolean = recordset.Supports( CursorOptions )`

La méthode **Supports** retourne une valeur booléenne indiquant si toutes les fonctionnalités identifiées par l'argument *CursorOptions* sont prises en charge par le fournisseur. Vous pouvez utiliser la méthode **Supports** pour déterminer les types de fonctionnalités pris en charge par un objet **Recordset**. Si l'objet **Recordset** prend en charge les fonctionnalités dont les constantes correspondantes se trouvent dans *CursorOptions*, la méthode **Supports** retourne la valeur **True**. Sinon, elle retourne la valeur **False**.

À l'aide de la méthode **Supports**, vous pouvez vérifier si l'objet **Recordset** peut ajouter de nouveaux enregistrements, utiliser des signets, utiliser la méthode **Find**, utiliser le défilement, utiliser la propriété **Index** et procéder à des mises à jour par lot. Pour obtenir une liste complète des constantes et de leur signification, consultez [CursorOptionEnum](cursoroptionenum.md).

Même si la méthode **Supports** retourne la valeur **True** pour une fonctionnalité donnée, rien ne garantit que le fournisseur puisse la fournir en toutes circonstances. La valeur retournée par la méthode **Supports** indique simplement si le fournisseur peut prendre en charge la fonctionnalité spécifiée, pour autant que certaines conditions soient remplies. Par exemple, la méthode **Supports** peut indiquer qu'un objet **Recordset** prend en charge les mises à jour, même si le curseur dépend d'une jointure de plusieurs tables  dont certaines colonnes ne sont pas modifiables.

