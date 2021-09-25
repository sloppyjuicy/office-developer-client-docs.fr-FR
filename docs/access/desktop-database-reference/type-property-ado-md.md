---
title: Type, propriété (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1c7b361a41fedc234d95d87a3002713bc3cf9853
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588916"
---
# <a name="type-property-ado-md"></a>Type, propriété (ADO MD)


**S’applique à** : Access 2013, Office 2013

Indique le type du membre actuel.

## <a name="return-values"></a>Valeurs de retour

Retourne une valeur [MemberTypeEnum](membertypeenum.md) et est en lecture seule.

## <a name="remarks"></a>Remarques

Cette propriété est uniquement prise en charge par les objets [Member](member-object-ado-md.md) appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

