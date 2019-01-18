---
title: Parent, propriété (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0c0eef638cb76676cd2287a34c0e4b17bd89c4d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699998"
---
# <a name="parent-property-ado-md"></a>Parent, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Indique le membre qui est le parent du membre actif dans une hiérarchie.

## <a name="return-values"></a>Valeurs de retour

Retourne un objet [Member](member-object-ado-md.md) et est en lecture seule.

## <a name="remarks"></a>Notes

Un membre au niveau supérieur d'une hiérarchie (racine) n'a aucun parent. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

