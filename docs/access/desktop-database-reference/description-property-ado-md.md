---
title: Description, property (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dd66e0288e20bcf38adefc2fcc30f1856ebf3e6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606870"
---
# <a name="description-property-ado-md"></a>Description, property (ADO MD)


**S’applique à**: Access 2013 | Office 2013

Retourne une explication textuelle de l'objet actif.

<<<<<<< Tête
## <a name="return-values"></a>Valeurs renvoyées
=======
## <a name="return-values"></a>Valeurs de retour
>>>>>>> master

Retourne une valeur de type **String** et est en lecture seule.

## <a name="remarks"></a>Notes

Pour les objets [Member](member-object-ado-md.md), la propriété **Description** s'applique uniquement aux membres de formule et de mesure. La propriété **Description** retourne une chaîne vide ("") pour tous les autres types de membres. Pour plus d'informations sur ces divers types de membres, consultez la propriété [Type](type-property-ado-md.md).

Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

