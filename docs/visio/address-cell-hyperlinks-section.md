---
title: Address, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438035"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="f5a7f-103">Address, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="f5a7f-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="f5a7f-104">Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.</span><span class="sxs-lookup"><span data-stu-id="f5a7f-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="f5a7f-105">Vous pouvez spécifier l’adresse comme chemin d’accès relatif basé sur  le chemin d’accès de base  défini pour le document dans la zone de **base Lien hypertexte** sous l’onglet Résumé de la boîte de dialogue Propriétés (cliquez sur l’onglet Fichier, cliquez sur **Info,** sur \*\* Propriétés \*\*, puis sur **Propriétés** avancées). </span><span class="sxs-lookup"><span data-stu-id="f5a7f-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="f5a7f-106">Si le document n’a pas de chemin de base, l’application utilise le chemin d’accès du document.</span><span class="sxs-lookup"><span data-stu-id="f5a7f-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="f5a7f-107">Si le document n’a pas encore été enregistré, le lien hypertexte n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="f5a7f-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5a7f-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5a7f-108">Remarks</span></span>

<span data-ttu-id="f5a7f-109">Vous pouvez également définir la valeur de la cellule Address dans la boîte de dialogue **Liens hypertexte** (cliquez sur **Lien hypertexte** sous l’onglet **Insertion**).</span><span class="sxs-lookup"><span data-stu-id="f5a7f-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="f5a7f-110">Pour obtenir une référence à la cellule Address à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f5a7f-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5a7f-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="f5a7f-111">Cell name:</span></span>  <br/> |<span data-ttu-id="f5a7f-112">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="f5a7f-112">Hyperlink.</span></span> <span data-ttu-id="f5a7f-113">*nom*  . Adresse où Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="f5a7f-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="f5a7f-114">*nom*  est le nom de la ligne de lien hypertexte</span><span class="sxs-lookup"><span data-stu-id="f5a7f-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="f5a7f-115">Pour obtenir une référence à la cellule Address par un nom à partir d’une autre formule ou d’un programme, à l’aide de la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="f5a7f-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f5a7f-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f5a7f-116">Section index:</span></span>  <br/> |<span data-ttu-id="f5a7f-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="f5a7f-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="f5a7f-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f5a7f-118">Row index:</span></span>  <br/> |<span data-ttu-id="f5a7f-119">**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f5a7f-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f5a7f-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f5a7f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f5a7f-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="f5a7f-121">**visHLinkAddress**</span></span> <br/> |
   

