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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417363"
---
# <a name="imapiforminfo--imapiprop"></a><span data-ttu-id="2ce7e-103">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2ce7e-103">IMAPIFormInfo : IMAPIProp</span></span>

  
  
<span data-ttu-id="2ce7e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ce7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ce7e-105">Donne aux applications clientes l’accès aux propriétés qui sont spécifiques à la définition de formulaire.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-105">Gives client applications access to properties that are particular to form definition.</span></span> <span data-ttu-id="2ce7e-106">En conservant les informations de formulaire dans un objet distinct, le fournisseur de bibliothèque de formulaires peut décrire un formulaire à un client sans l’activer.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-106">By keeping form information in a separate object, the form library provider can describe a form to a client without activating the form.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2ce7e-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2ce7e-107">Header file:</span></span>  <br/> |<span data-ttu-id="2ce7e-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="2ce7e-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="2ce7e-109">Exposé par :</span><span class="sxs-lookup"><span data-stu-id="2ce7e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2ce7e-110">Objets d’informations de formulaire</span><span class="sxs-lookup"><span data-stu-id="2ce7e-110">Form information objects</span></span>  <br/> |
|<span data-ttu-id="2ce7e-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2ce7e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ce7e-112">Fournisseurs de bibliothèques de formulaires</span><span class="sxs-lookup"><span data-stu-id="2ce7e-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="2ce7e-113">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2ce7e-113">Called by:</span></span>  <br/> |<span data-ttu-id="2ce7e-114">Applications clientes</span><span class="sxs-lookup"><span data-stu-id="2ce7e-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="2ce7e-115">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="2ce7e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2ce7e-116">IID_IMAPIFormInfo</span><span class="sxs-lookup"><span data-stu-id="2ce7e-116">IID_IMAPIFormInfo</span></span>  <br/> |
|<span data-ttu-id="2ce7e-117">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="2ce7e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2ce7e-118">LPMAPIFORMINFO</span><span class="sxs-lookup"><span data-stu-id="2ce7e-118">LPMAPIFORMINFO</span></span>  <br/> |
|<span data-ttu-id="2ce7e-119">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="2ce7e-119">Transaction model:</span></span>  <br/> |<span data-ttu-id="2ce7e-120">Non traduit</span><span class="sxs-lookup"><span data-stu-id="2ce7e-120">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2ce7e-121">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="2ce7e-121">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2ce7e-122">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="2ce7e-122">CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md) <br/> |<span data-ttu-id="2ce7e-123">Renvoie un pointeur vers l’ensemble complet des propriétés qu’un formulaire utilise.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-123">Returns a pointer to the complete set of properties that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="2ce7e-124">CalcVerbSet</span><span class="sxs-lookup"><span data-stu-id="2ce7e-124">CalcVerbSet</span></span>](imapiforminfo-calcverbset.md) <br/> |<span data-ttu-id="2ce7e-125">Renvoie un pointeur vers l’ensemble complet des verbes qu’un formulaire utilise.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-125">Returns a pointer to the complete set of verbs that a form uses.</span></span>  <br/> |
|[<span data-ttu-id="2ce7e-126">MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="2ce7e-126">MakeIconFromBinary</span></span>](imapiforminfo-makeiconfrombinary.md) <br/> |<span data-ttu-id="2ce7e-127">Crée une icône à partir d’une propriété d’icône d’un formulaire.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-127">Builds an icon from an icon property of a form.</span></span>  <br/> |
|[<span data-ttu-id="2ce7e-128">SaveForm</span><span class="sxs-lookup"><span data-stu-id="2ce7e-128">SaveForm</span></span>](imapiforminfo-saveform.md) <br/> |<span data-ttu-id="2ce7e-129">Enregistre une description d’un formulaire particulier dans un fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-129">Saves a description of a particular form in a configuration file.</span></span>  <br/> |
|[<span data-ttu-id="2ce7e-130">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="2ce7e-130">OpenFormContainer</span></span>](imapiforminfo-openformcontainer.md) <br/> |<span data-ttu-id="2ce7e-131">Renvoie un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé.</span><span class="sxs-lookup"><span data-stu-id="2ce7e-131">Returns a pointer to the form container in which a particular form is installed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ce7e-132">Remarques</span><span class="sxs-lookup"><span data-stu-id="2ce7e-132">Remarks</span></span>

<span data-ttu-id="2ce7e-133">Contrairement à la plupart des interfaces définies dans le fichier d’en-tête MapiForm.h, **IMAPIFormInfo** hérite de l’interface [IMAPIProp,](imapipropiunknown.md) car il exporte la plupart des informations de formulaire par le biais d’appels à la méthode [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="2ce7e-133">Unlike most interfaces defined in the MapiForm.h header file, **IMAPIFormInfo** inherits from the [IMAPIProp](imapipropiunknown.md) interface, because it exports most form information through calls to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ce7e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ce7e-134">See also</span></span>



[<span data-ttu-id="2ce7e-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="2ce7e-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

