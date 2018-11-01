---
title: Parent, propriété (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7beba341a2374e1868c67c8f7b4fab73c71c0ba8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880298"
---
# <a name="parent-property-ado-md"></a>Parent, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Indique le membre qui est le parent du membre actif dans une hiérarchie.

## <a name="return-values"></a>Valeurs de retour

Retourne un objet [Member](member-object-ado-md.md) et est en lecture seule.

## <a name="remarks"></a>Notes

Un membre au niveau supérieur d'une hiérarchie (racine) n'a aucun parent. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

