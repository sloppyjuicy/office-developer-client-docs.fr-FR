---
title: Move, méthode-ActiveX Data Objects (ADO)
TOCTitle: Move method (ADO)
ms:assetid: 1f858654-5fa3-273d-7cdc-574c5f09a420
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248982(v=office.15)
ms:contentKeyID: 48543645
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6c7db661e590bc21605d9c289b1de6d4ae9f46e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288833"
---
# <a name="move-method-ado"></a>Move, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Déplace la position de l’enregistrement actif dans un objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

*Recordset*. Déplacer *numRecords*, *Démarrer*

## <a name="parameters"></a>Paramètres

|Parameter|Description|
|:--------|:----------|
|*NumRecords* |Expression de type **Long** signée qui spécifie le nombre d'enregistrements dont la position de l'enregistrement actif sera déplacée.|
|*Début* |Facultatif. Valeur de type **String** ou **Variant** qui correspond à un signet. Vous pouvez également utiliser une valeur [BookmarkEnum](bookmarkenum.md).|

## <a name="remarks"></a>Remarques

La méthode **Move** est prise en charge sur tous les objets **Recordset**.

Si l'argument *NumRecords* est supérieur à zéro, la position de l'enregistrement actif est avancée (vers la fin du **jeu d'enregistrements**). Si l'argument *NumRecords* est inférieur à zéro, la position de l'enregistrement actif est déplacée vers l'arrière (vers le début du **jeu d'enregistrements**).

Si l'appel de la fonction **Move** déplace la position de l'enregistrement actif vers un point qui précède le premier enregistrement, ADO définit l'enregistrement actif à la position précédant le premier enregistrement de l'objet Recordset (la propriété[BOF](bof-eof-properties-ado.md) a la **valeur true**). Une tentative de déplacement vers l’arrière lorsque la propriété **BOF** a déjà la valeur **True** génère une erreur.

Si l’appel de la méthode **Move** déplace la position de l’enregistrement vers un point situé après le dernier enregistrement, ADO définit la position de l’enregistrement actif après le dernier enregistrement du jeu d’enregistrements (la propriété [EOF](bof-eof-properties-ado.md) a la valeur **True**). Une tentative de déplacement vers l’avant lorsque la propriété **EOF** a déjà la valeur **True** génère une erreur.

L'appel de la méthode **Move** à partir d'un objet **Recordset** vide génère une erreur.

Si vous passez l'argument *Début*, le déplacement est effectué par rapport à l'enregistrement affecté de ce signet, pour autant que l'objet **Recordset** prenne en charge les signets. S'il n'est pas spécifié, le déplacement est effectué par rapport à l'enregistrement actif.

Supposons que vous utilisiez la propriété [CacheSize](cachesize-property-ado.md) pour effectuer une mise en cache locale des enregistrements du fournisseur. Si vous passez un argument *NumRecords* qui déplace la position de l’enregistrement actif hors du groupe des enregistrements actuellement en cache, ADO extrait automatiquement un nouveau groupe d’enregistrements, à partir de l’enregistrement de destination. La propriété **CacheSize** détermine la taille du nouveau groupe extrait et l’enregistrement de destination est le premier enregistrement extrait.

Si l’objet **Recordset** peut être déplacé vers l’avant uniquement, un utilisateur peut néanmoins passer un argument *NbEnregistrements* inférieur à zéro, pour autant que la destination fasse partie du jeu actif d’enregistrements mis en cache. Si l’appel de la méthode **Move** déplace la position d’enregistrement actif vers un enregistrement placé avant le premier enregistrement mis en cache, une erreur se produit. Par conséquent, vous pouvez utiliser un cache d’enregistrements qui prend en charge le défilement bi-directionnel sur un fournisseur qui ne prend en charge que le défilement avant. Dans la mesure où les enregistrements mis en cache sont chargés en mémoire, évitez de mettre en cache plus d’enregistrements qu’il n’est nécessaire. Même si un objet **Recordset** avant seulement peut prendre en charge ce type de déplacement arrière, l’appel de la méthode [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) sur un objet **Recordset** avant seulement génère néanmoins une erreur.


> [!NOTE]
> [!REMARQUE] La prise en charge d'un déplacement arrière dans un objet **Recordset** avant seulement dépend de votre fournisseur et reste donc imprévisible. Si l'enregistrement actif a été placé après le dernier enregistrement de l'objet **Recordset**, un **déplacement** arrière est susceptible d'entraîner une position active incorrecte.


