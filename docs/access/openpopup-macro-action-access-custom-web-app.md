---
title: Action de Macro OpenPopup (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Ouvre le mode spécifié dans une fenêtre contextuelle.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781952"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a><span data-ttu-id="9993b-103">Action de Macro OpenPopup (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="9993b-103">OpenPopup Macro Action (Access custom web app)</span></span>

<span data-ttu-id="9993b-104">Ouvre le mode spécifié dans une fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="9993b-104">Opens the specified view in a popup window.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9993b-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="9993b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9993b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9993b-107">Syntax</span></span>

 <span data-ttu-id="9993b-108">**OpenPopup** (*Afficher*, *où =*, *Order By*)</span><span class="sxs-lookup"><span data-stu-id="9993b-108">**OpenPopup** (*View*, *Where=*, *Order By*)</span></span> 
  
<span data-ttu-id="9993b-109">L’action **OpenPopup** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="9993b-109">The **OpenPopup** action contains the following arguments.</span></span> 
  
|<span data-ttu-id="9993b-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="9993b-110">**Argument name**</span></span>|<span data-ttu-id="9993b-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9993b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9993b-112">*View*</span><span class="sxs-lookup"><span data-stu-id="9993b-112">*View*</span></span>  <br/> |<span data-ttu-id="9993b-113">Nom de la vue à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="9993b-113">The name of the view to open.</span></span>  <br/> |
| <span data-ttu-id="9993b-114">*Où =*</span><span class="sxs-lookup"><span data-stu-id="9993b-114">*Where=*</span></span>  <br/> |<span data-ttu-id="9993b-115">Clause SQL WHERE (sans le mot où) qui limite les enregistrements dans l’affichage.</span><span class="sxs-lookup"><span data-stu-id="9993b-115">A valid SQL WHERE clause (without the word WHERE) that restricts the records in the view.</span></span>  <br/> |
| <span data-ttu-id="9993b-116">*Order By*</span><span class="sxs-lookup"><span data-stu-id="9993b-116">*Order By*</span></span>  <br/> |<span data-ttu-id="9993b-117">Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs.</span><span class="sxs-lookup"><span data-stu-id="9993b-117">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords.</span></span> <span data-ttu-id="9993b-118">Par défaut, cet argument est vide.</span><span class="sxs-lookup"><span data-stu-id="9993b-118">By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9993b-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="9993b-119">Remarks</span></span>

<span data-ttu-id="9993b-120">La macro en cours se termine une fois que l’action **OpenPopup** est traitée.</span><span class="sxs-lookup"><span data-stu-id="9993b-120">The current macro ends once the **OpenPopup** action is processed.</span></span> 
  
<span data-ttu-id="9993b-121">Tout tri ou filtrage appliqué par l’utilisateur est effacé lors de l’action **OpenPopup** est appelée.</span><span class="sxs-lookup"><span data-stu-id="9993b-121">Any sorting or filtering applied by the user is cleared when the **OpenPopup** action is called.</span></span> 
  
<span data-ttu-id="9993b-122">L’argument *OrderBy (TriPar)* est le nom du champ ou des champs sur lesquels vous souhaitez trier les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="9993b-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="9993b-123">Lorsque vous utilisez plusieurs noms de champs, séparez les noms par une virgule (,).</span><span class="sxs-lookup"><span data-stu-id="9993b-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="9993b-124">Lorsque vous définissez l’argument *OrderBy* , les enregistrements sont triés par défaut par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="9993b-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  

