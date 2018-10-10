---
title: DeleteRecord, méthode (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d850234faf18a2bd6f3278ee4feade3aa3bb561
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469270"
---
# <a name="deleterecord-method-ado"></a><span data-ttu-id="7c92b-102">DeleteRecord, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="7c92b-102">DeleteRecord Method (ADO)</span></span>


<span data-ttu-id="7c92b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c92b-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="7c92b-104">Supprime une entité représentée par un objet [Record](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7c92b-104">Deletes a the entity represented by a [Record](record-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c92b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c92b-105">Syntax</span></span>

<span data-ttu-id="7c92b-106">*Enregistrement*. \**DeleteRecord \*\*\* Source*, *asynchrone*</span><span class="sxs-lookup"><span data-stu-id="7c92b-106">*Record*.\**DeleteRecord\*\*\*Source*, *Async*</span></span>

## <a name="parameters"></a><span data-ttu-id="7c92b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c92b-107">Parameters</span></span>

  - <span data-ttu-id="7c92b-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="7c92b-108">*Source*</span></span>

  - <span data-ttu-id="7c92b-p101">Facultatif. Valeur de type **String** contenant l’URL qui identifie l’entité (par exemple, le fichier ou le répertoire) à supprimer. Si le paramètre *Source* est omis ou spécifie une chaîne vide, l’entité représentée par l’objet [Record](record-object-ado.md) actif est supprimée. Si l’objet Record est un enregistrement de collection (propriété [RecordType](recordtype-property-ado.md) avec la valeur **adCollectionRecord**, tel qu’un répertoire) tous les enfants (par exemple les sous-répertoires) seront également supprimés.</span><span class="sxs-lookup"><span data-stu-id="7c92b-p101">Optional. A **String** value that contains a URL identifying the entity (for example, the file or directory) to be deleted. If *Source* is omitted or specifies an empty string, the entity represented by the current [Record](record-object-ado.md) is deleted. If the Record is a collection record ([RecordType](recordtype-property-ado.md) of **adCollectionRecord**, such as a directory) all children (for example, subdirectories) will also be deleted.</span></span>

  - <span data-ttu-id="7c92b-113">*Async*</span><span class="sxs-lookup"><span data-stu-id="7c92b-113">*Async*</span></span>

  - <span data-ttu-id="7c92b-p102">Facultatif. Valeur de type **Boolean**. Si sa valeur est **True**, spécifie que l'opération de suppression est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7c92b-p102">Optional. A **Boolean** value that, when **True**, specifies that the delete operation is asynchronous.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c92b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="7c92b-116">Remarks</span></span>

<span data-ttu-id="7c92b-117">Opérations sur l’objet représenté par cet **enregistrement** peuvent échouer une fois cette méthode terminée.</span><span class="sxs-lookup"><span data-stu-id="7c92b-117">Operations on the object represented by this **Record** may fail after this method completes.</span></span> <span data-ttu-id="7c92b-118">Après avoir appelé **DeleteRecord**, l' **enregistrement** doit être fermé car le comportement de l' **enregistrement** peut devenir imprévisible selon le moment où le fournisseur met à jour l' **enregistrement** de la source de données.</span><span class="sxs-lookup"><span data-stu-id="7c92b-118">After calling **DeleteRecord**, the **Record** should be closed because the behavior of the **Record** may become unpredictable depending upon when the provider updates the **Record** with the data source.</span></span>

<span data-ttu-id="7c92b-119">Si cet **enregistrement** a été obtenue à partir d’un [jeu d’enregistrements](recordset-object-ado.md), puis les résultats de cette opération ne seront pas reflétées immédiatement dans le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="7c92b-119">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), then the results of this operation will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="7c92b-120">Actualiser le **jeu d’enregistrements** en fermant et en ouvrant de nouveau ou en exécutant les méthodes **Recordset** [Requery](requery-method-ado.md)ou [Update](update-method-ado.md) et [Resync](resync-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="7c92b-120">Refresh the **Recordset** by closing and re-opening it, or by executing the **Recordset** [Requery](requery-method-ado.md), or [Update](update-method-ado.md) and [Resync](resync-method-ado.md) methods.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7c92b-p105">[!REMARQUE] Les URL qui utilisent le schéma http appellent automatiquement le <A href="microsoft-ole-db-provider-for-internet-publishing.md">fournisseur Microsoft OLE DB pour la publication Internet</A>. Pour plus d'informations, consultez <A href="absolute-and-relative-urls.md">URL absolues et relatives</A>.</span><span class="sxs-lookup"><span data-stu-id="7c92b-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


