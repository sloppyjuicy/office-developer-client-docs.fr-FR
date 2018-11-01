---
title: Informations d'erreurs liées au jeu d'enregistrements
TOCTitle: Recordset-Related Error Information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2df186db80515fdc9a7e77b8030d3ccd82ad793
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888698"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="fcd57-102">Informations d'erreurs liées au jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="fcd57-102">Recordset-Related Error Information</span></span>


<span data-ttu-id="fcd57-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcd57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fcd57-104">Au cours du traitement par lots, la propriété **Status** de l'objet **Recordset** fournit des informations sur chaque élément de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fcd57-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="fcd57-105">Avant la mise à jour d'un lot, la propriété **Status** de l'objet **Recordset** donne des indications concernant les enregistrements à ajouter, à modifier et à supprimer.</span><span class="sxs-lookup"><span data-stu-id="fcd57-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="fcd57-106">Après l'appel de **UpdateBatch**, la propriété **Status** indique la réussite ou l'échec de l'opération.</span><span class="sxs-lookup"><span data-stu-id="fcd57-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="fcd57-107">Lorsque vous passez d'un enregistrement à l'autre dans l'objet **Recordset**, la valeur de la propriété **Status** est modifiée afin de décrire le statut de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="fcd57-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

