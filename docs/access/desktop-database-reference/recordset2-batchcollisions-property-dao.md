---
title: Recordset2.BatchCollisions Property (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 07d6c25f-baf5-f7d6-d225-0447e0f78fe6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844993(v=office.15)
ms:contentKeyID: 48543085
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 204b66b120405522707da23bf093a311ca8c2625
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470886"
---
# <a name="recordset2batchcollisions-property-dao"></a><span data-ttu-id="04220-102">Recordset2.BatchCollisions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="04220-102">Recordset2.BatchCollisions Property (DAO)</span></span>


<span data-ttu-id="04220-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="04220-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="04220-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04220-104">Syntax</span></span>

<span data-ttu-id="04220-105">*expression* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="04220-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="04220-106">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="04220-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="04220-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="04220-107">Remarks</span></span>

<span data-ttu-id="04220-p101">Cette propriété contient un tableau de signets vers des lignes qui ont présenté un conflit au cours du dernier appel de la méthode **[Update](recordset2-update-method-dao.md)** par lot. La propriété **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** indique le nombre d'éléments présents dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="04220-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset2-update-method-dao.md)** call. The **[BatchCollisionCount](recordset2-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="04220-110">Si vous affectez à la propriété [**Bookmark**](recordset2-bookmark-property-dao.md) de l'objet **Recordset** de travail des valeurs de signet du tableau **BatchCollisions**, vous pouvez accéder à chaque enregistrement qui n'a pas pu achever la dernière opération de mise à jour par lot</span><span class="sxs-lookup"><span data-stu-id="04220-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="04220-p102">Après correction des enregistrements présentant des conflits, il est possible d'appeler à nouveau une méthode **Update** par lot. À ce stade, DAO tente d'exécuter une autre mise à jour par lot et la propriété **BatchCollisions** reflète à nouveau le jeu d'enregistrements ayant échoué à la deuxième tentative. Tous les enregistrements dont la mise à jour a réussi lors de la tentative précédente ne sont pas repris dans la tentative actuelle car leur propriété **[RecordStatus](recordset2-recordstatus-property-dao.md)** a désormais la valeur dbRecordUnmodified. Ce processus peut se poursuivre aussi longtemps que des conflits surviennent ou jusqu'à ce que vous abandonniez les mises à jour et fermiez le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="04220-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="04220-115">Ce tableau est recréé à chaque exécution d'une méthode **Update** par lot.</span><span class="sxs-lookup"><span data-stu-id="04220-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

