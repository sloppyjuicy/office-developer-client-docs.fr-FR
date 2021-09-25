---
title: AbsolutePage, propriété (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 15c4fe003acc3fbc76723c8d0dc271a75b5318d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569663"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage, propriété (ADO)

**S’applique à** : Access 2013, Office 2013

Indique la page sur laquelle se trouve l'enregistrement actif.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **long** de 1 au nombre de pages dans l’objet [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)), ou renvoie l’une des valeurs [PositionEnum.](positionenum.md)

## <a name="remarks"></a>Remarques

Cette propriété peut être utilisée pour identifier le numéro de page sur laquelle se trouve l'enregistrement actif. Elle utilise la propriété [PageSize](pagesize-property-ado.md) pour séparer logiquement le nombre total de jeux de lignes de l'objet **Recordset** en une série de pages, chacune possédant un nombre d'enregistrements égal à **PageSize** (à l'exception de la dernière page, qui peut comporter moins d'enregistrements). Le fournisseur doit prendre en charge les fonctions appropriées pour que cette propriété soit disponible.

Lors de l'extraction ou de la définition de la propriété **AbsolutePage**, ADO utilise conjointement les propriétés [AbsolutePosition](absoluteposition-property-ado.md) et [PageSize](pagesize-property-ado.md), de la manière suivante :

- Pour extraire **AbsolutePage**, ADO commence par extraire **AbsolutePosition**, qu'il divise par la valeur **PageSize**.

- Pour définir **AbsolutePage**, ADO déplace **AbsolutePosition** de la manière suivante : il multiplie **PageSize** par la nouvelle valeur **AbsolutePage** et y ajoute 1. Par conséquent, la position actuelle dans le jeu **d’enregistrements** après la définition de **AbsolutePage** est le premier enregistrement de cette page.

Comme la propriété **AbsolutePosition**, la propriété **AbsolutePage** est en base 1 et est égale à 1 lorsque l'enregistrement actif correspond au premier enregistrement du **Recordset**. Définissez cette propriété pour accéder au premier enregistrement d'une page déterminée. Obtenez le nombre total de pages à partir de la propriété **PageCount**.

