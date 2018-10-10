---
title: Requery, méthode (ADO)
TOCTitle: Requery Method (ADO)
ms:assetid: 1062d907-979f-020a-b2ed-94e11c0e7d08
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248871(v=office.15)
ms:contentKeyID: 48543292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3fde13d923a67ca995cdb3e7f59a327e82a9688
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471122"
---
# <a name="requery-method-ado"></a>Requery, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013



Cette méthode met à jour les données d'un objet [Recordset](recordset-object-ado.md) en réexécutant la requête sur laquelle l'objet est basé.

## <a name="syntax"></a>Syntaxe

*jeu d’enregistrements*. Actualiser les *Options*

## <a name="parameter"></a>Paramètre

  - *Options*

  - Facultatif. Masque de bits contenant des valeurs [ExecuteOptionEnum](executeoptionenum.md) et [CommandTypeEnum](commandtypeenum.md) affectant cette opération.


> [!NOTE]
> <P>Si <EM>Options</EM> a la valeur <STRONG>adAsyncExecute</STRONG>, cette opération est exécutée de façon asynchrone et un événement <A href="willchangerecordset-and-recordsetchangecomplete-events-ado.md">RecordsetChangeComplete</A> est déclenché lorsqu’elle est terminée.</P>



Les valeurs **adExecuteNoRecords** ou **adExecuteStream** de l'énumération **ExecuteOpenEnum** ne doivent pas être utilisées avec **Requery**.

## <a name="remarks"></a>Notes

Faites appel à la méthode **Requery** pour actualiser tout le contenu d'un objet **Recordset** à partir de la base de données en réexécutant la commande d'origine et en extrayant les données une seconde fois. L'appel de cette méthode revient à appeler successivement les méthodes [Close](close-method-ado.md) et [Open](open-method-ado-recordset.md). Si vous modifiez l'enregistrement actif ou que vous ajoutez un nouvel enregistrement, une erreur se produit.

Lorsque l’objet **Recordset** est ouvert, les propriétés qui définissent la nature du curseur ([CursorType](cursortype-property-ado.md), [LockType](locktype-property-ado.md), [MaxRecords](maxrecords-property-ado.md), etc.) sont en lecture seule. Ainsi, la méthode **Requery** ne peut actualiser que le curseur actif. Pour changer des propriétés du curseur et afficher les résultats ainsi obtenus, vous devez faire appel à la méthode [Close](close-method-ado.md) afin que les propriétés soient à nouveau en lecture-écriture. Vous pouvez alors changer les paramètres des propriétés et appeler la méthode [Open](open-method-ado-recordset.md) pour rouvrir le curseur.

