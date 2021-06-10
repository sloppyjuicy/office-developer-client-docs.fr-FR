---
title: 'Chapitre 5 : Mise à jour et persistance des données'
TOCTitle: 'Chapter 5: Updating and persisting data'
ms:assetid: 77acb763-1c60-1945-791d-3e83d684fb0d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249493(v=office.15)
ms:contentKeyID: 48545732
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18dd63acd733624fba522ee7382f305d34019905
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296429"
---
# <a name="chapter-5-updating-and-persisting-data"></a><span data-ttu-id="2bbb0-102">Chapitre 5 : Mise à jour et persistance des données</span><span class="sxs-lookup"><span data-stu-id="2bbb0-102">Chapter 5: Updating and persisting data</span></span>

<span data-ttu-id="2bbb0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2bbb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2bbb0-p101">Les chapitres précédents ont présenté la marche à suivre dans ADO pour accéder aux données d'une source de données, pour se déplacer dans les données et pour les modifier. Si l'application est évidemment conçue pour permettre aux utilisateurs de modifier ces données, il est tout aussi nécessaire qu'ils puissent enregistrer ces modifications. Pour ce faire, deux méthodes sont possibles : enregistrer les modifications de l'objet **Recordset** de façon persistante dans un fichier à l'aide de la méthode **Save** ou renvoyer ces modifications à la source de données, où elles seront stockées, avec les méthodes **Update** ou **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="2bbb0-p101">The preceding chapters have discussed how to use ADO to get to data in a data source, how to move around in the data, and even how to edit the data. Of course, if the goal of your application is to allow users to make changes to the data, you will need to understand how to save those changes. You can either persist the **Recordset** changes to a file using the **Save** method, or you can send the changes back to the data source for storage using the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="2bbb0-p102">Dans les chapitres précédents, vous avez appris à modifier les données dans plusieurs lignes de l'objet **Recordset**. Deux points méritent d'être soulignés quant à l'ajout, la suppression et la modification des lignes de données dans ADO.</span><span class="sxs-lookup"><span data-stu-id="2bbb0-p102">In the preceding chapters, you changed the data in several rows of the **Recordset**. ADO supports two basic notions relating to the addition, deletion, and modification of rows of data.</span></span>

<span data-ttu-id="2bbb0-p103">D'une part, il faut savoir que les modifications ne sont pas directement appliquées à l'objet **Recordset**. Elles sont d'abord enregistrées dans un *tampon de copie* interne. Si vous décidez d'annuler les modifications, elles sont supprimées. Si vous décidez de les conserver, elles sont alors appliquées à l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2bbb0-p103">The first notion is that changes aren't immediately made to the **Recordset**; instead, they are made to an internal *copy buffer*. If you decide you don't want the changes, the modifications in the copy buffer are discarded. If you decide to keep the changes, the changes in the copy buffer are applied to the **Recordset**.</span></span>

<span data-ttu-id="2bbb0-p104">D'autre part, les modifications sont propagées à la source de données dès que vous achevez le traitement d'une ligne (mode de mise à jour *immédiate*) ou toutes les modifications apportées à un groupe de lignes sont collectées et conservées jusqu'à ce que vous acheviez le traitement de ce groupe (mode de mise à jour *par lot*). C'est la propriété **LockType** qui détermine quand ces modifications sont appliquées à la source de données sous-jacente. **adLockOptimistic** ou **adLockPessimistic** spécifie le mode de mise à jour immédiate tandis que **adLockBatchOptimistic** spécifie le mode de mise à jour par lot. La propriété **CursorLocation** peut déterminer les paramètres disponibles pour la propriété **LockType**. Par exemple, le paramètre **adLockPessimistic** n'est pas pris en charge si la propriété **CursorLocation** a la valeur **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="2bbb0-p104">The second notion is that changes are either propagated to the data source as soon as you declare the work on a row complete (that is, *immediate* mode), or all changes to a set of rows are collected until you declare the work for the set complete (that is, *batch* mode). The **LockType** property determines when the changes are made to the underlying data source. **adLockOptimistic** or **adLockPessimistic** specifies immediate mode, while **adLockBatchOptimistic** specifies batch mode. The **CursorLocation** property can affect which **LockType** settings are available. For instance, the **adLockPessimistic** setting is not supported if the **CursorLocation** property is set to **adUseClient**.</span></span>

<span data-ttu-id="2bbb0-p105">En mode de mise à jour immédiate, chaque appel de la méthode **Update** propage les modifications à la source de données. En mode de mise à jour par lot, chaque appel de la méthode **Update** ou chaque déplacement de la position de ligne active enregistre les modifications dans le tampon de copie, mais seule la méthode **UpdateBatch** propage les modifications à la source de données.</span><span class="sxs-lookup"><span data-stu-id="2bbb0-p105">In immediate mode, each invocation of the **Update** method propagates the changes to the data source. In batch mode, each invocation of **Update** or movement of the current row position saves the changes to the copy buffer, but only the **UpdateBatch** method propagates the changes to the data source.</span></span>

<span data-ttu-id="2bbb0-119">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="2bbb0-119">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="2bbb0-120">Updating data (ADO)</span><span class="sxs-lookup"><span data-stu-id="2bbb0-120">Updating data (ADO)</span></span>](updating-data.md)
- [<span data-ttu-id="2bbb0-121">Persisting data (ADO)</span><span class="sxs-lookup"><span data-stu-id="2bbb0-121">Persisting data (ADO)</span></span>](persisting-data.md)
