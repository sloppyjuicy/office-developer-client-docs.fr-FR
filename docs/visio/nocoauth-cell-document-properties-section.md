---
title: NoCoauth, cellule (Section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f2095c9-ce09-48f7-b160-c9822d96a96c
description: Indique si un document stocké sur un serveur Microsoft SharePoint 2013 ou sur Microsoft OneDrive peut être modifié par plusieurs auteurs simultanément dans une session de co-création.
ms.openlocfilehash: a20c3a5aa1392e0e6c3bef124f536b91b9642f47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789171"
---
# <a name="nocoauth-cell-document-properties-section"></a><span data-ttu-id="2a997-103">NoCoauth, cellule (Section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="2a997-103">NoCoauth Cell (Document Properties Section)</span></span>

<span data-ttu-id="2a997-104">Indique si un document stocké sur un serveur Microsoft SharePoint 2013 ou sur Microsoft OneDrive peut être modifié par plusieurs auteurs simultanément dans une session de co-création.</span><span class="sxs-lookup"><span data-stu-id="2a997-104">Sets whether a document stored on a Microsoft SharePoint 2013 server or Microsoft OneDrive can be edited by multiple authors simultaneously in a coauthoring session.</span></span>
  
|<span data-ttu-id="2a997-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="2a997-105">**Value**</span></span>|<span data-ttu-id="2a997-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a997-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2a997-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2a997-107">TRUE</span></span>  <br/> |<span data-ttu-id="2a997-108">Le document ne peut pas être attribué et est verrouillé pour modification lorsqu’il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="2a997-108">The document cannot be coauthored and is locked for editing when open.</span></span>  <br/> |
|<span data-ttu-id="2a997-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2a997-109">FALSE</span></span>  <br/> |<span data-ttu-id="2a997-110">Le document peut être attribué.</span><span class="sxs-lookup"><span data-stu-id="2a997-110">The document can be coauthored.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a997-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="2a997-111">Remarks</span></span>

<span data-ttu-id="2a997-112">Pour obtenir une référence à la cellule **NoCoauth** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="2a997-112">To get a reference to the **NoCoauth** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a997-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2a997-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2a997-114">NoCoauth</span><span class="sxs-lookup"><span data-stu-id="2a997-114">NoCoauth</span></span>  <br/> |
   
<span data-ttu-id="2a997-115">Pour obtenir une référence à la cellule **NoCoauth** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2a997-115">To get a reference to the **NoCoauth** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a997-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2a997-116">Section index:</span></span>  <br/> |<span data-ttu-id="2a997-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2a997-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2a997-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2a997-118">Row index:</span></span>  <br/> |<span data-ttu-id="2a997-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="2a997-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="2a997-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2a997-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2a997-121">**visDocNoCoauth**</span><span class="sxs-lookup"><span data-stu-id="2a997-121">**visDocNoCoauth**</span></span> <br/> |
   

