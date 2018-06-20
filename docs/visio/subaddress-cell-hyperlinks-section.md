---
title: SubAddress, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm985
localization_priority: Normal
ms.assetid: 949448fd-0f85-b56a-945e-1da0e48609e8
description: Indique un emplacement au sein du document cible vers lequel établir un lien.
ms.openlocfilehash: 0509b9b6a708924b5aeb69f16f3f4cd99573cc0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789841"
---
# <a name="subaddress-cell-hyperlinks-section"></a><span data-ttu-id="11913-103">SubAddress, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="11913-103">SubAddress Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="11913-104">Indique un emplacement au sein du document cible vers lequel établir un lien.</span><span class="sxs-lookup"><span data-stu-id="11913-104">Specifies a location within the target document to link to.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11913-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="11913-105">Remarks</span></span>

<span data-ttu-id="11913-106">Par exemple, si la cellule Address est « Drawing1.vsdx », la cellule SubAddress peut spécifier un nom de page tel que « Page 3 ».</span><span class="sxs-lookup"><span data-stu-id="11913-106">For example, if the Address cell is "Drawing1.vsdx", the SubAddress cell can specify a page name such as "Page-3".</span></span> <span data-ttu-id="11913-107">Si la cellule Address est le fichier Microsoft Excel « Samples.xlsx », la valeur de cette cellule peut être une feuille de calcul ou une plage dans une feuille de calcul, tel que « Fonctions de feuille de calcul » ou « Sheet1 ! A1 : D10 ».</span><span class="sxs-lookup"><span data-stu-id="11913-107">If the Address cell is the Microsoft Excel file "Samples.xlsx", the value of this cell can be a worksheet or range within a worksheet, such as "Worksheet Functions" or "Sheet1!A1:D10".</span></span> <span data-ttu-id="11913-108">Si la cellule Address est «http://www.microsoft.com/office/», la valeur de cette cellule peut être un point d’ancrage nommé dans le document, tel que « solutions ».</span><span class="sxs-lookup"><span data-stu-id="11913-108">If the Address cell is "http://www.microsoft.com/office/", the value of this cell can be a named anchor within the document, such as "solutions".</span></span>
  
<span data-ttu-id="11913-109">Vous pouvez également définir la valeur de cette cellule dans la boîte de dialogue **liens hypertexte** (dans le groupe **liens** sous l’onglet **Insertion** , cliquez sur **lien hypertexte**).</span><span class="sxs-lookup"><span data-stu-id="11913-109">You can also set the value of this cell in the **Hyperlinks** dialog box (in the **Links** group on the **Insert** tab, click **Hyperlink**).</span></span>
  
<span data-ttu-id="11913-110">Pour obtenir une référence à la cellule SubAddress par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="11913-110">To get a reference to the SubAddress cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11913-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="11913-111">Cell name:</span></span>  <br/> | <span data-ttu-id="11913-112">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="11913-112">Hyperlink.</span></span>  <span data-ttu-id="11913-113">*nom* . SubAddress où le lien hypertexte *.name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="11913-113">*name*  .SubAddress where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="11913-114">Pour obtenir une référence à la cellule **SubAddress** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="11913-114">To get a reference to the **SubAddress** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="11913-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="11913-115">Section index:</span></span>  <br/> |<span data-ttu-id="11913-116">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="11913-116">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="11913-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="11913-117">Row index:</span></span>  <br/> |<span data-ttu-id="11913-118">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="11913-118">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="11913-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="11913-119">Cell index:</span></span>  <br/> |<span data-ttu-id="11913-120">**visHLinkSubAddress**</span><span class="sxs-lookup"><span data-stu-id="11913-120">**visHLinkSubAddress**</span></span> <br/> |
   

