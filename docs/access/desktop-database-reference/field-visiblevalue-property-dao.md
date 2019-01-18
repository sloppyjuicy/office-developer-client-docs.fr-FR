---
title: Propriété Field.VisibleValue (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1b3e1b6ec6cd34112f0ba1d84101390bbd400f82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712455"
---
# <a name="fieldvisiblevalue-property-dao"></a>Propriété Field.VisibleValue (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . VisibleValue

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Cette propriété contient la valeur du champ se trouvant actuellement dans la base de données sur le serveur. Pendant une mise à jour par lot optimiste, une collision peut se produire, si un deuxième client a modifié le même champ et enregistrement entre le moment où le premier client a récupéré les données et la première tentative de mise à jour par le premier client. Lorsque cela se produit, la valeur définie par le deuxième client est accessible grâce à cette propriété.

