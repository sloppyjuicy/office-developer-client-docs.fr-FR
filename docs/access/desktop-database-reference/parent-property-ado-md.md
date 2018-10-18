---
title: Parent, propriété (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603335"
---
# <a name="parent-property-ado-md"></a>Parent, propriété (ADO MD)


**S’applique à**: Access 2013 | Office 2013

Indique le membre qui est le parent du membre actif dans une hiérarchie.

<<<<<<< Tête
## <a name="return-values"></a>Valeurs renvoyées
=======
## <a name="return-values"></a>Valeurs de retour
>>>>>>> master

Retourne un objet [Member](member-object-ado-md.md) et est en lecture seule.

## <a name="remarks"></a>Notes

Un membre au niveau supérieur d'une hiérarchie (racine) n'a aucun parent. Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

