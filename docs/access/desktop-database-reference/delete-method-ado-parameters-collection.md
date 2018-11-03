---
title: DELETE, méthode (Collection de paramètres ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b18a09d6a0c9d6a6ad8e9f579068c4f6d7162d1f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944871"
---
# <a name="delete-method-ado-parameters-collection"></a>DELETE, méthode (Collection de paramètres ADO)


**S’applique à**: Access 2013, Office 2013


Supprime un objet de la collection [Parameters](parameters-collection-ado.md).

## <a name="syntax"></a>Syntaxe

*Paramètres*. Supprimer *l’Index*

## <a name="parameters"></a>Paramètres

- *Index*

  - Valeur de type **String** contenant le nom de l'objet que vous voulez supprimer ou la position ordinale (index) de l'objet dans la collection.

## <a name="remarks"></a>Notes

L'utilisation de la méthode **Delete** sur une collection permet de supprimer l'un des objets figurant dans cette collection. Cette méthode est uniquement disponible pour la collection **Parameters** d'un objet [Command](command-object-ado.md). Vous devez utiliser la propriété [Name](parameter-object-ado.md) de l'objet [Parameter](name-property-ado.md) ou son index de collection lorsque vous appelez la méthode **Delete**; une variable objet ne constitue pas un argument valide.

