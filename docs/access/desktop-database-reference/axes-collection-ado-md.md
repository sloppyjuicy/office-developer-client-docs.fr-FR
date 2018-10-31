---
title: Axes, collection (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 612a78d8ac99a070f133fd3804f5b69c8093d47c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862598"
---
# <a name="axes-collection-ado-md"></a>Axes, collection (ADO MD)


**S’applique à**: Access 2013 | Office 2013

Contient les objets [Axis](axis-object-ado-md.md) qui définissent un ensemble de cellules.

## <a name="remarks"></a>Remarques

Un objet [Cellset](cellset-object-ado-md.md) contient une collection **Axes**. Une fois l' **ensemble de cellules** ouvert, cette collection renferme au moins un **axe**. Reportez-vous à la rubrique consacrée à l'objet [Axis](axis-object-ado-md.md) pour une explication plus détaillée de l'utilisation des objets **Axis**.


> [!NOTE]
> [!REMARQUE] L'axe de filtrage d'un **ensemble de cellules** ne figure pas dans la collection **Axes**. Reportez-vous à la rubrique consacrée à la propriété [FilterAxis](filteraxis-property-ado-md.md) pour plus d'informations.



**Axes** est une collection ADO standard. Avec les propriétés et méthodes d'une collection, vous pouvez :

  - Obtenir le nombre d'objets d'une collection à l'aide de la propriété [Count](count-property-ado.md).

  - Renvoyer un objet de la collection à l'aide de la propriété [Item](item-property-ado.md) par défaut.

  - Mettre à jour les objets de la collection à partir du fournisseur à l'aide de la méthode [Refresh](refresh-method-ado.md).

