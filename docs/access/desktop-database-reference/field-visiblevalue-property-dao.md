---
title: Field.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 892c7b41a692f353ee7e5bdd2191f6e21b8b4cf2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469846"
---
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue Property (DAO)


**S’applique à**: Access 2013 | Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . VisibleValue

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Cette propriété contient la valeur du champ se trouvant actuellement dans la base de données sur le serveur. Pendant une mise à jour par lot optimiste, une collision peut se produire, si un deuxième client a modifié le même champ et enregistrement entre le moment où le premier client a récupéré les données et la première tentative de mise à jour par le premier client. Lorsque cela se produit, la valeur définie par le deuxième client est accessible grâce à cette propriété.

