---
title: PageCount, propriété (ADO)
TOCTitle: PageCount property (ADO)
ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15)
ms:contentKeyID: 48546609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: aab5455e4fd54316a2ef9af22b5322f85eb3a4e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558141"
---
# <a name="pagecount-property-ado"></a>PageCount, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le nombre de pages de données que contient l'objet [Recordset](recordset-object-ado.md).

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur de type **Long** qui indique le nombre de pages dans le **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **PageCount** pour déterminer le nombre de pages que contient l’objet **Recordset**. Les *Pages* sont des groupes d’enregistrements dont la taille est égale à la valeur de la propriété [PageSize](pagesize-property-ado.md). Même si la dernière page est incomplète et que le nombre d’enregistrements qu’elle contient est inférieur à la valeur de **PageSize**, elle est considérée comme une page supplémentaire dans la valeur **PageCount**. Si l’objet **Recordset** ne prend pas en charge cette propriété, la valeur sera -1, pour indiquer que la propriété **PageCount** ne peut pas être déterminée.

Pour plus d'informations sur les fonctionnalités relatives aux pages, voir les propriétés **PageSize** et [AbsolutePage](absolutepage-property-ado.md).

