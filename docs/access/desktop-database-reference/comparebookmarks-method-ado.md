---
title: CompareBookmarks, méthode (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0820d7efbc4dc742879fa454a49f91e99e1b7981
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928879"
---
# <a name="comparebookmarks-method-ado"></a>CompareBookmarks, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Compare deux signets et retourne une indication de leurs valeurs relatives.

## <a name="syntax"></a>Syntaxe

*résultat* = *jeu d’enregistrements*. CompareBookmarks (*Bookmark1*, *Bookmark2*)

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur [CompareEnum](compareenum.md) qui indique la position de ligne relative de deux enregistrements représentée par leur signet.

## <a name="parameters"></a>Paramètres

  - *Bookmark1*

  - Signet de la première ligne.

  - *Bookmark2*

  - Signet de la seconde ligne.

## <a name="remarks"></a>Notes

Les signets doivent s'appliquer au même objet [Recordset](recordset-object-ado.md) ou à un objet **Recordset** et à son [clone](clone-method-ado.md). Vous ne pouvez pas comparer correctement des signets issus d'objets **Recordset** différents, même s'ils ont été créés à partir de la même source ou commande. Vous ne pouvez pas non plus comparer des signets d'un objet **Recordset** dont le fournisseur sous-jacent ne prend pas en charge les comparaisons.

Un signet constitue l'identification unique d'une ligne dans un objet **Recordset**. Utilisez la propriété [Bookmark](bookmark-property-ado.md) de la ligne active pour obtenir son signet.

Comme le type de données d'un signet est propre au fournisseur, ADO l'expose en tant que type Variant. Par exemple, les signets SQL Server sont de type DBTYPE\_R8 (Double). ADO l'expose en tant que type Variant avec le sous-type Double.

Lorsqu'il compare des signets, ADO ne tente aucune forme de conversion forcée. Les valeurs sont tout simplement passées au fournisseur lors de la comparaison. Si les signets passés à la méthode **CompareBookmarks** sont stockés dans des variables de types différents, cela peut générer une erreur d'incompatibilité de type indiquant que les arguments n'ont pas le type approprié, qu'ils sont en dehors de la plage acceptable ou qu'ils sont en conflit.

Un signet qui n'est pas valide ni correctement formé génère une erreur.

