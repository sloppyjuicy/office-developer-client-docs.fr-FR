---
title: Mise à jour de données (référence de base de données du bureau Access)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70ca34183d135c6907a185984b02b394776bfda4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944220"
---
# <a name="updating-data"></a><span data-ttu-id="05b8d-102">Mise à jour des données</span><span class="sxs-lookup"><span data-stu-id="05b8d-102">Updating data</span></span>


<span data-ttu-id="05b8d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05b8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05b8d-104">Le comportement et les fonctionnalités de mise à jour dépendent, pour une large part, du mode de mise à jour (type de verrou), du type de curseur, et de l'emplacement du curseur.</span><span class="sxs-lookup"><span data-stu-id="05b8d-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="05b8d-p101">Utilisez la méthode **Update** pour enregistrer toutes les modifications apportées à l'enregistrement actif d'un objet **Recordset** depuis l'appel de la méthode **AddNew** ou depuis la modification des valeurs des champs d'un enregistrement existant. L'objet **Recordset** doit prendre en charge les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="05b8d-p101">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="05b8d-p102">Si l'objet **Recordset** prend en charge les mises à jour par lot, il est possible d'enregistrer dans un cache local les modifications apportées à un ou plusieurs enregistrements jusqu'à ce que vous appeliez la méthode **UpdateBatch**. Si vous êtes en train de modifier l'enregistrement actif ou d'ajouter un nouvel enregistrement lorsque vous appelez la méthode **UpdateBatch**, ADO appelle automatiquement la méthode **Update** pour enregistrer toutes les modifications en cours de l'enregistrement actif avant de transmettre les modifications par lot au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="05b8d-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="05b8d-109">L'enregistrement actif reste actif après l'appel des méthodes **Update** ou **UpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="05b8d-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="05b8d-110">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="05b8d-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="05b8d-111">Mode immédiat</span><span class="sxs-lookup"><span data-stu-id="05b8d-111">Immediate mode</span></span>](immediate-mode.md)
- [<span data-ttu-id="05b8d-112">Traitement des transactions</span><span class="sxs-lookup"><span data-stu-id="05b8d-112">Transaction processing</span></span>](transaction-processing.md)
- [<span data-ttu-id="05b8d-113">Mode de traitement par lots (ADO)</span><span class="sxs-lookup"><span data-stu-id="05b8d-113">Batch mode (ADO)</span></span>](batch-mode.md)

