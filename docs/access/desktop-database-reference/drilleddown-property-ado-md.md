---
title: DrilledDown, propriété (ADO MD)
TOCTitle: DrilledDown property (ADO MD)
ms:assetid: 1dfe728f-8da2-1d2b-7361-8689a0b088b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248972(v=office.15)
ms:contentKeyID: 48543610
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d521176eeb2ac2e83ef05d05d3572dfba543812
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931000"
---
# <a name="drilleddown-property-ado-md"></a>DrilledDown, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Indique si aucun enfant ne suit immédiatement le membre sur un axe.

## <a name="return-values"></a>Valeurs de retour

Retourne une valeur de type **Boolean** et est en lecture seule. **DrilledDown** retourne la valeur **True** s'il n'existe aucun membre enfant du membre actuel sur l'axe. **DrilledDown** retourne la valeur **False** s'il existe au moins un membre enfant du membre actuel sur l'axe.

## <a name="remarks"></a>Notes

Utilisez la propriété **DrilledDown** pour déterminer s'il existe au moins un enfant de ce membre sur l'axe situé immédiatement après lui. Ces informations sont utiles lors de l'affichage du membre.

Cette propriété est uniquement prise en charge par les objets [Member](member-object-ado-md.md) appartenant à un objet [Position](position-object-ado-md.md). Une erreur survient lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Level](level-object-ado-md.md).

