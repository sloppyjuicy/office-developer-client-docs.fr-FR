---
title: Axes, collection (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c88bf27f406a439d051112afb9abf94697a13b12
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922230"
---
# <a name="axes-collection-ado-md"></a>Axes, collection (ADO MD)


**S’applique à**: Access 2013, Office 2013

Contient les objets [Axis](axis-object-ado-md.md) qui définissent un ensemble de cellules.

## <a name="remarks"></a>Remarques

Un objet [Cellset](cellset-object-ado-md.md) contient une collection **Axes**. Une fois l' **ensemble de cellules** ouvert, cette collection renferme au moins un **axe**. Reportez-vous à la rubrique consacrée à l'objet [Axis](axis-object-ado-md.md) pour une explication plus détaillée de l'utilisation des objets **Axis**.


> [!NOTE]
> [!REMARQUE] L'axe de filtrage d'un **ensemble de cellules** ne figure pas dans la collection **Axes**. Reportez-vous à la rubrique consacrée à la propriété [FilterAxis](filteraxis-property-ado-md.md) pour plus d'informations.



**Axes** est une collection ADO standard. Avec les propriétés et méthodes d'une collection, vous pouvez :

  - Obtenir le nombre d'objets d'une collection à l'aide de la propriété [Count](count-property-ado.md).

  - Renvoyer un objet de la collection à l'aide de la propriété [Item](item-property-ado.md) par défaut.

  - Mettre à jour les objets de la collection à partir du fournisseur à l'aide de la méthode [Refresh](refresh-method-ado.md).

