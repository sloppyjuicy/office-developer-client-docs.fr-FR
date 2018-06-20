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
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788026"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="97b50-103">Address, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="97b50-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="97b50-104">Indique une adresse d’URL, un nom de fichier ou un chemin d’accès UNC auxquels accéder.</span><span class="sxs-lookup"><span data-stu-id="97b50-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="97b50-105">Vous pouvez spécifier l’adresse comme un chemin d’accès relatif basé sur le chemin d’accès de base défini pour le document dans la zone **base de lien hypertexte** sous l’onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur l’onglet **fichier** , cliquez sur **Info**** propriétés ** puis cliquez sur **Propriétés avancées**).</span><span class="sxs-lookup"><span data-stu-id="97b50-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click ** Properties **, and then click **Advanced Properties**).</span></span> <span data-ttu-id="97b50-106">Si le document n’a aucun chemin d’accès de base, l’application utilise le chemin d’accès du document.</span><span class="sxs-lookup"><span data-stu-id="97b50-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="97b50-107">Si le document n’a pas été enregistré, le lien hypertexte est indéfini.</span><span class="sxs-lookup"><span data-stu-id="97b50-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97b50-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="97b50-108">Remarks</span></span>

<span data-ttu-id="97b50-109">Vous pouvez également définir la valeur de la cellule Address dans la boîte de dialogue **liens hypertexte** (cliquez sur le **lien hypertexte** sous l’onglet **Insertion** ).</span><span class="sxs-lookup"><span data-stu-id="97b50-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="97b50-110">Pour obtenir une référence à la cellule Address par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="97b50-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97b50-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="97b50-111">Cell name:</span></span>  <br/> |<span data-ttu-id="97b50-112">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="97b50-112">Hyperlink.</span></span> <span data-ttu-id="97b50-113">*nom* . Adresse où un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="97b50-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="97b50-114">*nom* est le nom de la ligne hyperlink</span><span class="sxs-lookup"><span data-stu-id="97b50-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="97b50-115">Pour obtenir une référence à la cellule Address par un nom à partir d’une autre formule ou d’un programme, à l’aide de la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="97b50-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="97b50-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="97b50-116">Section index:</span></span>  <br/> |<span data-ttu-id="97b50-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="97b50-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="97b50-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="97b50-118">Row index:</span></span>  <br/> |<span data-ttu-id="97b50-119">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="97b50-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="97b50-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="97b50-120">Cell index:</span></span>  <br/> |<span data-ttu-id="97b50-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="97b50-121">**visHLinkAddress**</span></span> <br/> |
   

