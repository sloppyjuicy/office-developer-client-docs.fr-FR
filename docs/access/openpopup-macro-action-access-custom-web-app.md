---
title: OpenPopup, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Ouvre l'affichage spécifié dans une fenêtre contextuelle.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308112"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="074f9-103">OpenPopup, action de macro (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="074f9-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="074f9-104">Ouvre l'affichage spécifié dans une fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="074f9-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="074f9-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="074f9-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="074f9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="074f9-107">Syntax</span></span>

 <span data-ttu-id="074f9-108">**OpenPopup** (*View*, *Where =*, *order by*)</span><span class="sxs-lookup"><span data-stu-id="074f9-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="074f9-109">L'action **OpenPopup** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="074f9-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="074f9-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="074f9-110">**Argument name**</span></span>|<span data-ttu-id="074f9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="074f9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="074f9-112">*View*</span><span class="sxs-lookup"><span data-stu-id="074f9-112">*View*</span></span>  <br/> |<span data-ttu-id="074f9-113">Nom de la vue à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="074f9-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="074f9-114">*Où =*</span><span class="sxs-lookup"><span data-stu-id="074f9-114">*Where=*</span></span>  <br/> |<span data-ttu-id="074f9-115">Une clause SQL WHERE valide (sans le mot WHERE) qui limite les enregistrements dans l'affichage.</span><span class="sxs-lookup"><span data-stu-id="074f9-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="074f9-116">*Trier par*</span><span class="sxs-lookup"><span data-stu-id="074f9-116">*Order By*</span></span>  <br/> |<span data-ttu-id="074f9-117">Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs.</span><span class="sxs-lookup"><span data-stu-id="074f9-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="074f9-118">Par défaut, cet argument est vide.</span><span class="sxs-lookup"><span data-stu-id="074f9-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="074f9-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="074f9-119">Remarks</span></span>

<span data-ttu-id="074f9-120">La macro active se termine une fois l'action **OpenPopup** traitée.</span><span class="sxs-lookup"><span data-stu-id="074f9-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="074f9-121">Tout tri ou filtrage appliqué par l'utilisateur est effacé lors de l'appel de l'action **OpenPopup** .</span><span class="sxs-lookup"><span data-stu-id="074f9-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="074f9-122">L'argument *orderby* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="074f9-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="074f9-123">Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="074f9-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="074f9-124">Lorsque vous définissez l'argument *orderby* , les enregistrements sont triés par défaut dans l'ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="074f9-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

