---
title: Children, propriété (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57049e0e68e4620664687cd261881af953de189f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875209"
---
# <a name="children-property-ado-md"></a>Children, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Renvoie une collection d'objets [Member](members-collection-ado-md.md) dont l'objet [Member](member-object-ado-md.md) actif est le parent dans la hiérarchie.

## <a name="return-values"></a>Valeurs de retour

Retourne la collection **Members** et est en lecture seule.

## <a name="remarks"></a>Notes

La propriété **Children** contient une collection **Members** dont le **membre** actuel est le parent hiérarchique. Les objets **Member** de niveau feuille n'ont aucun membre enfant dans la collection **Members**. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

