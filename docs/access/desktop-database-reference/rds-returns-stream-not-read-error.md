---
title: Retour d'une erreur de type « Flux non lu » par RDS
TOCTitle: RDS Returns "Stream Not Read" Error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 312d6f7e29a7573237bf8e4ddab17b9f8796cc4b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870015"
---
# <a name="rds-returns-stream-not-read-error"></a><span data-ttu-id="e371e-102">RDS renvoie \"flux non lu\" erreur</span><span class="sxs-lookup"><span data-stu-id="e371e-102">RDS Returns \"Stream Not Read\" Error</span></span>


<span data-ttu-id="e371e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e371e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e371e-p101">« L'objet flux ne peut pas être lu car il est vide, ou la position actuelle se situe à la fin du flux. Pour les flux non vides, définissez la position actuelle à l'aide de la propriété Position. Pour savoir si un flux est vide, utilisez la propriété Size ».</span><span class="sxs-lookup"><span data-stu-id="e371e-p101">"The Stream object could not be read because it is empty, or the current position is at the end of the Stream. For non-empty Streams, set the current position with the Position property. To determine if a Stream is empty, check the Size property."</span></span>

<span data-ttu-id="e371e-p102">L'obtention de l'erreur précédente peut être le résultat d'une tentative d'utilisation d'une requête hiérarchique paramétrée sur http. Or, RDS ne permet pas d'utiliser à distance les hiérarchies paramétrées.</span><span class="sxs-lookup"><span data-stu-id="e371e-p102">If you get the error above, it may be a result of trying to use a parameterized hierarchical query over http. RDS does not permit you to remote parameterized hierarchies.</span></span>

