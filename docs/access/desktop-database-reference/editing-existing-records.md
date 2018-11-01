---
title: Modification d'enregistrements existants
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c500f89b0f16062e43ace45f55eab9a593d071a2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884232"
---
# <a name="editing-existing-records"></a><span data-ttu-id="4b047-102">Modification d'enregistrements existants</span><span class="sxs-lookup"><span data-stu-id="4b047-102">Editing Existing Records</span></span>


<span data-ttu-id="4b047-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b047-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b047-p101">Pour modifier des enregistrements existants, allez dans la ligne que vous souhaitez modifier et changez la propriété **Value** des champs à modifier.Pour en savoir plus sur la propriété **Field** de l'objet **Field**, reportez-vous au [Chapitre 3 : Examen des données](chapter-3-examining-data.md). Selon le type de votre curseur, utilisez les méthodes **Update** ou **UpdateBatch** pour renvoyer les modifications à la source de données. Pour en savoir plus, reportez-vous au [Chapitre 5 : Mise à jour et conservation des données](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="4b047-p101">To edit existing records, move to the row you want to edit and change the **Value** property of the fields you want to change. For more information about the **Field** object's **Value** property, see [Chapter 3: Examining Data](chapter-3-examining-data.md). Depending on your cursor type, you will use **Update** or **UpdateBatch** to send changes back to the data source. For more information, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

<span data-ttu-id="4b047-p102">L'utilisation d'une procédure stockée avec un objet de commande est généralement plus efficace pour réaliser des mises à jour, ainsi que d'autres opérations, car une procédure stockée ne nécessite pas la création d'un curseur. Pour en savoir plus sur les curseurs, reportez-vous au [Chapitre 8 : Présentation des curseurs et des verrous](chapter-8-understanding-cursors-and-locks.md).</span><span class="sxs-lookup"><span data-stu-id="4b047-p102">It is usually more efficient to use a stored procedure with a command object to perform updates, as well as to perform other operations, because a stored procedure does not require the creation of a cursor. For more information about cursors, see [Chapter 8: Understanding Cursors and Locks](chapter-8-understanding-cursors-and-locks.md).</span></span>

