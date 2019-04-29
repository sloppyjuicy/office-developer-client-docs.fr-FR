---
title: ChangeView, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Vous pouvez utiliser l'action ChangeView pour naviguer entre les vues en place.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425357"
---
# <a name="changeview-macro-action-access-custom-web-app"></a><span data-ttu-id="adaf1-103">ChangeView, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="adaf1-103">ChangeView Macro Action (Access custom web app)</span></span>

<span data-ttu-id="adaf1-104">Vous pouvez utiliser l'action **ChangeView** pour naviguer entre les vues en place.</span><span class="sxs-lookup"><span data-stu-id="adaf1-104">You can use the **ChangeView** action to navigate between views in place.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="adaf1-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="adaf1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="adaf1-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="adaf1-107">Setting</span></span>

<span data-ttu-id="adaf1-108">L'action **ChangeView** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="adaf1-108">The **ChangeView** action has the following arguments.</span></span> 
  
|<span data-ttu-id="adaf1-109">**Argument de l'action**</span><span class="sxs-lookup"><span data-stu-id="adaf1-109">**Action argument**</span></span>|<span data-ttu-id="adaf1-110">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="adaf1-110">**Required**</span></span>|<span data-ttu-id="adaf1-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="adaf1-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="adaf1-112">Table</span><span class="sxs-lookup"><span data-stu-id="adaf1-112">Table</span></span>  <br/> |<span data-ttu-id="adaf1-113">Oui</span><span class="sxs-lookup"><span data-stu-id="adaf1-113">Yes</span></span>  <br/> |<span data-ttu-id="adaf1-114">Nom de la table à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="adaf1-114">The name of the table to open.</span></span>  <br/> |
|<span data-ttu-id="adaf1-115">View</span><span class="sxs-lookup"><span data-stu-id="adaf1-115">View</span></span>  <br/> |<span data-ttu-id="adaf1-116">Oui</span><span class="sxs-lookup"><span data-stu-id="adaf1-116">Yes</span></span>  <br/> |<span data-ttu-id="adaf1-117">Nom de la vue à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="adaf1-117">The name of the view to open.</span></span>  <br/> |
|<span data-ttu-id="adaf1-118">Où</span><span class="sxs-lookup"><span data-stu-id="adaf1-118">Where</span></span>  <br/> |<span data-ttu-id="adaf1-119">Non</span><span class="sxs-lookup"><span data-stu-id="adaf1-119">No</span></span>  <br/> |<span data-ttu-id="adaf1-120">Spécifié, remplace la condition Where de la source de l'enregistrement de l'objet.</span><span class="sxs-lookup"><span data-stu-id="adaf1-120">If specified, replaces the Where condition of the object record source.</span></span>  <br/> |
|<span data-ttu-id="adaf1-121">Trier par</span><span class="sxs-lookup"><span data-stu-id="adaf1-121">Order By</span></span>  <br/> |<span data-ttu-id="adaf1-122">Non</span><span class="sxs-lookup"><span data-stu-id="adaf1-122">No</span></span>  <br/> |<span data-ttu-id="adaf1-123">Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs.</span><span class="sxs-lookup"><span data-stu-id="adaf1-123">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="adaf1-124">Par défaut, cet argument est vide.</span><span class="sxs-lookup"><span data-stu-id="adaf1-124">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="adaf1-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="adaf1-125">Remarks</span></span>

<span data-ttu-id="adaf1-126">Tout tri ou filtrage appliqué par l'utilisateur est effacé lors de l'appel de l'action **ChangeView** .</span><span class="sxs-lookup"><span data-stu-id="adaf1-126">Any sorting or filtering applied by the user is cleared when the **ChangeView** action is called.</span></span> 
  
<span data-ttu-id="adaf1-127">L'argument *orderby* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="adaf1-127">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="adaf1-128">Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="adaf1-128">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="adaf1-129">Lorsque vous définissez l'argument *orderby* , les enregistrements sont triés par défaut dans l'ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="adaf1-129">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

