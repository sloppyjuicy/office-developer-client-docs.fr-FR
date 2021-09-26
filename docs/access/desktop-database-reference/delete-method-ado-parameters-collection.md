---
title: Delete, méthode (collection Parameters ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 30545ef12b5f794985b4925fe242e360ed1576f5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622381"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete, méthode (collection Parameters ADO)

**S’applique à** : Access 2013, Office 2013

Supprime un objet de la collection [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Syntaxe

*Paramètres*. Supprimer un *index*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Index* |Valeur de type **String** contenant le nom de l'objet que vous voulez supprimer ou la position ordinale (index) de l'objet dans la collection.|

## <a name="remarks"></a>Remarques

L’utilisation de la méthode **Delete** sur une collection permet de supprimer l’un des objets figurant dans cette collection. Cette méthode est uniquement disponible pour la collection **Parameters** d’un objet [Command](command-object-ado.md). Vous devez utiliser la propriété [Name](name-property-ado.md) de l’objet [Parameter](parameter-object-ado.md) ou son index de collection lorsque vous appelez la méthode **Delete** ; une variable objet ne constitue pas un argument valide.

