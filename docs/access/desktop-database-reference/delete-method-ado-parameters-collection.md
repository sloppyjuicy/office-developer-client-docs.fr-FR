---
title: Delete, méthode (collection Parameters ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e519d40a081b132cd09030e9ba97de9e8987af99
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881957"
---
# <a name="delete-method-ado-parameters-collection"></a>Delete, méthode (collection Parameters ADO)


**S’applique à**: Access 2013, Office 2013


Supprime un objet de la collection [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Syntaxe

*Paramètres*. Supprimer *l’Index*

## <a name="parameters"></a>Paramètres

  - *Index*

  - Valeur de type **String** contenant le nom de l'objet que vous voulez supprimer ou la position ordinale (index) de l'objet dans la collection.

## <a name="remarks"></a>Notes

L'utilisation de la méthode **Delete** sur une collection permet de supprimer l'un des objets figurant dans cette collection. Cette méthode est uniquement disponible pour la collection **Parameters** d'un objet [Command](command-object-ado.md). Vous devez utiliser la propriété [Name](parameter-object-ado.md) de l'objet [Parameter](name-property-ado.md) ou son index de collection lorsque vous appelez la méthode **Delete**; une variable objet ne constitue pas un argument valide.

