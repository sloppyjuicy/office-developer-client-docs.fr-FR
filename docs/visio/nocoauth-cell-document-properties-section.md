---
title: NoCoauth Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Définit si un document stocké sur un serveur Microsoft SharePoint 2013 ou Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-création.
ms.openlocfilehash: a76e2d3b2c3cf6e99e37596b016f448b0be56fd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319438"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="9a3cb-103">NoCoauth Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="9a3cb-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="9a3cb-104">Définit si un document stocké sur un serveur Microsoft SharePoint 2013 ou Microsoft OneDrive peut être modifié simultanément par plusieurs auteurs dans une session de co-création.</span><span class="sxs-lookup"><span data-stu-id="9a3cb-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="9a3cb-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9a3cb-105">**Value**</span></span>|<span data-ttu-id="9a3cb-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a3cb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9a3cb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9a3cb-107">TRUE</span></span>  <br/> |<span data-ttu-id="9a3cb-108">Le document ne peut pas être co-créé et ne peut pas être modifié lorsqu'il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="9a3cb-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="9a3cb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9a3cb-109">FALSE</span></span>  <br/> |<span data-ttu-id="9a3cb-110">Le document peut être co-créé.</span><span class="sxs-lookup"><span data-stu-id="9a3cb-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9a3cb-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a3cb-111">Remarks</span></span>

<span data-ttu-id="9a3cb-112">Pour obtenir une référence à la cellule **NoCoauth** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="9a3cb-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a3cb-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="9a3cb-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9a3cb-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="9a3cb-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="9a3cb-115">Pour obtenir une référence à la cellule **NoCoauth** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="9a3cb-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9a3cb-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9a3cb-116">Section index:</span></span>  <br/> |<span data-ttu-id="9a3cb-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="9a3cb-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9a3cb-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9a3cb-118">Row index:</span></span>  <br/> |<span data-ttu-id="9a3cb-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="9a3cb-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="9a3cb-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9a3cb-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9a3cb-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="9a3cb-121">**visDocNoCoauth**</span></span> <br/> |
   

