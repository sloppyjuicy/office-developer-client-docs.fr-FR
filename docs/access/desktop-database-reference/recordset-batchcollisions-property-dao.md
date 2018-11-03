---
title: Propriété Recordset.BatchCollisions (DAO)
TOCTitle: BatchCollisions Property
ms:assetid: 53e5572b-770c-9ea5-31a5-984abdf66faa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194079(v=office.15)
ms:contentKeyID: 48544881
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c151868e349621d964f61058cfe82458764cf443
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929089"
---
# <a name="recordsetbatchcollisions-property-dao"></a><span data-ttu-id="45949-102">Propriété Recordset.BatchCollisions (DAO)</span><span class="sxs-lookup"><span data-stu-id="45949-102">Recordset.BatchCollisions property (DAO)</span></span>


<span data-ttu-id="45949-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="45949-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="45949-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45949-104">Syntax</span></span>

<span data-ttu-id="45949-105">*expression* . BatchCollisions</span><span class="sxs-lookup"><span data-stu-id="45949-105">*expression* .BatchCollisions</span></span>

<span data-ttu-id="45949-106">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="45949-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="45949-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="45949-107">Remarks</span></span>

<span data-ttu-id="45949-p101">Cette propriété contient un tableau de signets permettant d'accéder aux lignes qui ont subi des collisions lors de la dernière opération **[Update](recordset-update-method-dao.md)** par lot. La propriété **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** indique le nombre d'éléments contenus dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="45949-p101">This property contains an array of bookmarks to rows that encountered a collision during the last attempted batch **[Update](recordset-update-method-dao.md)** call. The **[BatchCollisionCount](recordset-batchcollisioncount-property-dao.md)** property indicates the number of elements in the array.</span></span>

<span data-ttu-id="45949-110">Si vous définissez la propriété **[Bookmark](recordset-object-dao.md)** de l'objet **[Recordset](recordset-bookmark-property-dao.md)** de travail sur des signets du tableau **BatchCollisions**, vous pouvez accéder à chaque enregistrement dont la dernière opération Update par lot a échoué.</span><span class="sxs-lookup"><span data-stu-id="45949-110">If you set the working **[Recordset](recordset-object-dao.md)** object's **[Bookmark](recordset-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch-mode Update operation.</span></span>

<span data-ttu-id="45949-p102">Une fois les enregistrements en collision corrigés, il est possible de rappeler la méthode **Update** en mode par lot. À ce stade, DAO tente d'exécuter une autre mise à jour par lot et la propriété **BatchCollisions** indique à nouveau le jeu d'enregistrements dont la seconde tentative a échoué. Les enregistrements dont la tentative précédente a réussi ne sont pas envoyés dans la tentative en cours, car ils possèdent à présent la propriété **[RecordStatus](recordset-recordstatus-property-dao.md)** dbRecordUnmodified. Ce processus peut se poursuivre jusqu'à ce que toutes les collisions soient résolues ou que vous abandonniez les mises à jour et fermiez le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="45949-p102">After the collision records are corrected, you can call the batch mode **Update** method again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, as they now have a **[RecordStatus](recordset-recordstatus-property-dao.md)** property of dbRecordUnmodified. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

<span data-ttu-id="45949-115">Ce tableau est recréé à chaque exécution d'une méthode **Update** par lot.</span><span class="sxs-lookup"><span data-stu-id="45949-115">This array is re-created each time you execute a batch-mode **Update** method.</span></span>

