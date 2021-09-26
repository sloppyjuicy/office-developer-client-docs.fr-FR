---
title: CompareBookmarks, méthode (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3439cb1a15d98c8e0b882ef8ba0bfd3e934f689a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612280"
---
# <a name="comparebookmarks-method-ado"></a>CompareBookmarks, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Compare deux signets et retourne une indication de leurs valeurs relatives.

## <a name="syntax"></a>Syntaxe

*result*  =  *recordset*. CompareBookmarks(*Bookmark1*, *Bookmark2*)

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur [CompareEnum](compareenum.md) qui indique la position de ligne relative de deux enregistrements représentée par leur signet.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Bookmark1* |Signet de la première ligne.|
|*Bookmark2* |Signet de la seconde ligne.|

## <a name="remarks"></a>Remarques

Les signets doivent s'appliquer au même objet [Recordset](recordset-object-ado.md) ou à un objet **Recordset** et à son [clone](clone-method-ado.md). Vous ne pouvez pas comparer correctement des signets issus d'objets **Recordset** différents, même s'ils ont été créés à partir de la même source ou commande. Vous ne pouvez pas non plus comparer des signets d'un objet **Recordset** dont le fournisseur sous-jacent ne prend pas en charge les comparaisons.

Un signet constitue l'identification unique d'une ligne dans un objet **Recordset**. Utilisez la propriété [Bookmark](bookmark-property-ado.md) de la ligne active pour obtenir son signet.

Comme le type de données d'un signet est propre au fournisseur, ADO l'expose en tant que type Variant. Par exemple, SQL Server signets sont de type DBTYPE \_ R8 (Double). ADO l'expose en tant que type Variant avec le sous-type Double.

Lorsqu'il compare des signets, ADO ne tente aucune forme de conversion forcée. Les valeurs sont tout simplement passées au fournisseur lors de la comparaison. Si les signets passés à la méthode **CompareBookmarks** sont stockés dans des variables de types différents, cela peut générer une erreur d'incompatibilité de type indiquant que les arguments n'ont pas le type approprié, qu'ils sont en dehors de la plage acceptable ou qu'ils sont en conflit.

Un signet qui n'est pas valide ni correctement formé génère une erreur.

