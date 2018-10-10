---
title: Description, property (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29c6723d710fcf3a8114fb4460326d87261c3fc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469789"
---
# <a name="description-property-ado-md"></a>Description, property (ADO MD)


**S’applique à**: Access 2013 | Office 2013

Retourne une explication textuelle de l'objet actif.

## <a name="return-values"></a>Valeurs de retour

Retourne une valeur de type **String** et est en lecture seule.

## <a name="remarks"></a>Notes

Pour les objets [Member](member-object-ado-md.md), la propriété **Description** s'applique uniquement aux membres de formule et de mesure. La propriété **Description** retourne une chaîne vide ("") pour tous les autres types de membres. Pour plus d'informations sur ces divers types de membres, consultez la propriété [Type](type-property-ado-md.md).

Cette propriété est uniquement prise en charge par les objets **Member** appartenant à un objet [Level](level-object-ado-md.md). Une erreur se produit lorsque cette propriété est référencée à partir des objets **Member** appartenant à un objet [Position](position-object-ado-md.md).

