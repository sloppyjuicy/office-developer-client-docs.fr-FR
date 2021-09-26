---
title: Objet Cellset (ADO MD)
TOCTitle: Cellset object (ADO MD)
ms:assetid: 28d4b3b9-f907-9ec0-00e1-9666c887cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249047(v=office.15)
ms:contentKeyID: 48543869
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 147ca9fb41c0c8d9209da4737c9e0cd680845559
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622528"
---
# <a name="cellset-object-ado-md"></a>Objet Cellset (ADO MD)

**S’applique à** : Access 2013, Office 2013

Représente les résultats d'une requête multidimensionnelle. Il s'agit d'une collection de cellules sélectionnées dans des cubes ou d'autres ensembles de cellules.

## <a name="remarks"></a>Remarques

Les données d'un **ensemble de cellules** sont extraites à l'aide d'un accès direct de type matrice. Vous pouvez détailler un certain membre pour obtenir les données le concernant. Par exemple, le code suivant renvoie la légende du premier membre de la première position sur le premier axe d'un ensemble de cellules appelé cst :

`cst.Axes(0).Positions(0).Members(0).Caption`

La notion de cellule active est inexistante dans un ensemble de cellules. En revanche, la propriété [Item](item-property-ado-md-cellset.md) extrait un objet [Cell](cell-object-ado-md.md) spécifique de l'ensemble de cellules. Les arguments de la propriété **Item** déterminent la cellule à extraire. Vous pouvez spécifier la valeur ordinale unique d'une cellule. Vous pouvez également extraire des cellules via leur numéro de position sur chaque axe de l'ensemble de cellules. Pour plus d'informations sur l'extraction des cellules, reportez-vous à la rubrique consacrée à la propriété [Item](item-property-ado-md-cellset.md).

Avec les collections, méthodes et propriétés d'un objet **Cellset**, vous pouvez :

  - Associer une connexion ouverte à un objet **Cellset** en définissant sa propriété [ActiveConnection](activeconnection-property-ado-md.md).

  - Exécuter une requête multidimensionnelle et en extraire les résultats à l'aide de la méthode [Open](open-method-ado-md.md).

  - Extraire une **cellule** de l' **ensemble de cellules** à l'aide de la propriété [Item](item-property-ado-md-cellset.md).

  - Renvoyer les objets [Axis](axis-object-ado-md.md) définissant l' **ensemble de cellules** à l'aide de la collection [Axes](axes-collection-ado-md.md).

  - Extraire les informations relatives aux dimensions utilisées pour filtrer les données de l' **ensemble de cellules** à l'aide de la propriété [FilterAxis](filteraxis-property-ado-md.md).

  - Renvoyer ou spécifier la requête utilisée pour définir l' **ensemble de cellules** à l'aide de la propriété [Source](source-property-ado-md.md).

  - Renvoyer l'état actuel de l' **ensemble de cellules** (ouvert, fermé, en cours d'exécution ou de connexion) à l'aide de la propriété [State](state-property-ado-md.md).

  - Fermer un **ensemble de cellules** ouvert à l'aide de la méthode [Close](close-method-ado-md.md).

  - Extraire les informations spécifiques au fournisseur relatives à l' **ensemble de cellules** à l'aide de la collection ADO standard [Properties](properties-collection-ado.md).

