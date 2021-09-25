---
title: Parent, propriété (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 858978b45fd8ee687dd60619bbdb59c0eef01f68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617901"
---
# <a name="parent-property-ado-md"></a>Parent, propriété (ADO MD)


**S’applique à** : Access 2013, Office 2013

Indique le membre qui est le parent du membre actif dans une hiérarchie.

## <a name="return-values"></a>Valeurs de retour

Retourne un objet [Member](member-object-ado-md.md) et est en lecture seule.

## <a name="remarks"></a>Remarques

Un membre au niveau supérieur d’une hiérarchie (racine) n’a aucun parent. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

