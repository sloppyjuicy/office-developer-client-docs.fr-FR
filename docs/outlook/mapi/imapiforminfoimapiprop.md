---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575909"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="dbf70-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dbf70-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="dbf70-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbf70-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbf70-105">Fournit l’accès client applications aux propriétés qui sont spécifiques à la définition du formulaire.</span><span class="sxs-lookup"><span data-stu-id="dbf70-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="dbf70-106">En conservant les informations d’un formulaire dans un objet séparé, le fournisseur de bibliothèque formulaire permet de décrire un formulaire à un client sans activer le formulaire.</span><span class="sxs-lookup"><span data-stu-id="dbf70-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dbf70-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="dbf70-107">Header file:</span></span>  <br/> |<span data-ttu-id="dbf70-108">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="dbf70-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="dbf70-109">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="dbf70-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="dbf70-110">Objets d’informations de formulaire</span><span class="sxs-lookup"><span data-stu-id="dbf70-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="dbf70-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="dbf70-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="dbf70-112">Fournisseurs de bibliothèques de formulaires</span><span class="sxs-lookup"><span data-stu-id="dbf70-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="dbf70-113">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="dbf70-113">Called by:</span></span>  <br/> |<span data-ttu-id="dbf70-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="dbf70-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="dbf70-115">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="dbf70-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="dbf70-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="dbf70-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="dbf70-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="dbf70-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="dbf70-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="dbf70-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="dbf70-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="dbf70-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="dbf70-120">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="dbf70-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="dbf70-121">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="dbf70-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="dbf70-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="dbf70-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="dbf70-123">Retourne un pointeur vers l’ensemble complet des propriétés qui utilise un formulaire.</span><span class="sxs-lookup"><span data-stu-id="dbf70-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="dbf70-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="dbf70-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="dbf70-125">Retourne un pointeur vers l’ensemble complet des verbes qui utilise un formulaire.</span><span class="sxs-lookup"><span data-stu-id="dbf70-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="dbf70-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="dbf70-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="dbf70-127">Crée une icône à partir d’une propriété de l’icône d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="dbf70-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="dbf70-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="dbf70-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="dbf70-129">Enregistre une description d’un formulaire particulier dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="dbf70-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="dbf70-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="dbf70-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="dbf70-131">Retourne un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé.</span><span class="sxs-lookup"><span data-stu-id="dbf70-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbf70-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="dbf70-132">Remarks</span></span>

<span data-ttu-id="dbf70-133">Contrairement à la plupart des interfaces définies dans le fichier d’en-tête MapiForm.h, **IMAPIFormInfo** hérite de l’interface [IMAPIProp](imapipropiunknown.md) , car il exporte la plupart des informations d’un formulaire via des appels à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf70-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dbf70-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbf70-134">See also</span></span>



[<span data-ttu-id="dbf70-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="dbf70-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

