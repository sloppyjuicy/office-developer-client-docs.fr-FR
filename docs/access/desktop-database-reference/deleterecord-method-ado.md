---
title: DeleteRecord, méthode (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293993"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="f50ae-102">DeleteRecord, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="f50ae-102">DeleteRecord method (ADO)</span></span>

<span data-ttu-id="f50ae-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f50ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f50ae-104">Supprime une entité représentée par un objet [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f50ae-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f50ae-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f50ae-105">Syntax</span></span>

<span data-ttu-id="f50ae-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span><span class="sxs-lookup"><span data-stu-id="f50ae-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="f50ae-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f50ae-107">Parameters</span></span>

|<span data-ttu-id="f50ae-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f50ae-108">Parameter</span></span>|<span data-ttu-id="f50ae-109">Description</span><span class="sxs-lookup"><span data-stu-id="f50ae-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f50ae-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="f50ae-110">*Source*</span></span> |<span data-ttu-id="f50ae-p101">Facultatif. Valeur de type **String** contenant l’URL qui identifie l’entité (par exemple, le fichier ou le répertoire) à supprimer. Si le paramètre *Source* est omis ou spécifie une chaîne vide, l’entité représentée par l’objet [Record](record-object-ado.md) actif est supprimée. Si l’objet Record est un enregistrement de collection (propriété [RecordType](recordtype-property-ado.md) avec la valeur **adCollectionRecord**, tel qu’un répertoire) tous les enfants (par exemple les sous-répertoires) seront également supprimés.</span><span class="sxs-lookup"><span data-stu-id="f50ae-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>|
|<span data-ttu-id="f50ae-115">*Async*</span><span class="sxs-lookup"><span data-stu-id="f50ae-115">*Async*</span></span> |<span data-ttu-id="f50ae-p102">Facultatif. Valeur de type **Boolean**. Si sa valeur est **True**, spécifie que l'opération de suppression est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="f50ae-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f50ae-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="f50ae-118">Remarks</span></span>

<span data-ttu-id="f50ae-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span><span class="sxs-lookup"><span data-stu-id="f50ae-p103">Operations on the object represented by this **Record** may fail after this method completes. After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="f50ae-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f50ae-121">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="f50ae-122">**Actualisez le recordset** en le fermant et en le ré ouvrant, ou en exécutant la méthode [Requery](requery-method-ado.md)ou [Update](update-method-ado.md) et [Resync.](resync-method-ado.md) </span><span class="sxs-lookup"><span data-stu-id="f50ae-122">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>

> [!NOTE]
> <span data-ttu-id="f50ae-123">Les URL qui utilisent le schéma http appellent automatiquement le [fournisseur Microsoft OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="f50ae-123">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="f50ae-124">Pour plus d’informations, voir [URL absolues et relatives.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="f50ae-124">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


