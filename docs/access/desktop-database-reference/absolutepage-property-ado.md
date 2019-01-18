---
title: AbsolutePage, propriété (ADO)
TOCTitle: AbsolutePage property (ADO)
ms:assetid: b6e5daac-cc21-0aa6-9119-a973595762bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249881(v=office.15)
ms:contentKeyID: 48547288
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a0ad4caa6e31b6de39904016cd848e12690f72e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705259"
---
# <a name="absolutepage-property-ado"></a>AbsolutePage, propriété (ADO)

**S’applique à**: Access 2013, Office 2013

Indique la page sur laquelle se trouve l'enregistrement actif.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de **type Long** comprise entre 1 et le nombre de pages dans l’objet [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) ou renvoie une des valeurs de [PositionEnum](positionenum.md) .

## <a name="remarks"></a>Notes

Cette propriété peut être utilisée pour identifier le numéro de page sur laquelle se trouve l'enregistrement actif. Elle utilise la propriété [PageSize](pagesize-property-ado.md) pour séparer logiquement le nombre total de jeux de lignes de l'objet **Recordset** en une série de pages, chacune possédant un nombre d'enregistrements égal à **PageSize** (à l'exception de la dernière page, qui peut comporter moins d'enregistrements). Le fournisseur doit prendre en charge les fonctions appropriées pour que cette propriété soit disponible.

Lors de l'extraction ou de la définition de la propriété **AbsolutePage**, ADO utilise conjointement les propriétés [AbsolutePosition](absoluteposition-property-ado.md) et [PageSize](pagesize-property-ado.md), de la manière suivante :

- Pour extraire **AbsolutePage**, ADO commence par extraire **AbsolutePosition**, qu'il divise par la valeur **PageSize**.

- Pour définir **AbsolutePage**, ADO déplace **AbsolutePosition** de la manière suivante : il multiplie **PageSize** par la nouvelle valeur **AbsolutePage** et y ajoute 1. Par conséquent, la position actuelle dans le **jeu d’enregistrements** une fois la valeur **AbsolutePage** est le premier enregistrement de cette page.

Comme la propriété **AbsolutePosition**, la propriété **AbsolutePage** est en base 1 et est égale à 1 lorsque l'enregistrement actif correspond au premier enregistrement du **Recordset**. Définissez cette propriété pour accéder au premier enregistrement d'une page déterminée. Obtenez le nombre total de pages à partir de la propriété **PageCount**.

