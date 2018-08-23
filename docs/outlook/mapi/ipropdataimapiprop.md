---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c320b2c42b9a14c6dc428fc3df59991528cdbe36
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592569"
---
# <a name="ipropdata--imapiprop"></a><span data-ttu-id="fe3df-103">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fe3df-103">IPropData : IMAPIProp</span></span>

  
  
<span data-ttu-id="fe3df-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fe3df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fe3df-105">Offre la possibilité de récupérer et de modifier l’accès pour les propriétés d’un objet.</span><span class="sxs-lookup"><span data-stu-id="fe3df-105">Provides the ability to retrieve and change the access for an object's properties.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe3df-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fe3df-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe3df-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fe3df-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fe3df-108">Exposés par :</span><span class="sxs-lookup"><span data-stu-id="fe3df-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="fe3df-109">Objet de données de propriété</span><span class="sxs-lookup"><span data-stu-id="fe3df-109">Property data object</span></span>  <br/> |
|<span data-ttu-id="fe3df-110">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fe3df-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="fe3df-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="fe3df-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="fe3df-112">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="fe3df-112">Called by:</span></span>  <br/> |<span data-ttu-id="fe3df-113">Fournisseurs de services et applications clientes</span><span class="sxs-lookup"><span data-stu-id="fe3df-113">Service providers and client applications</span></span>  <br/> |
|<span data-ttu-id="fe3df-114">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="fe3df-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fe3df-115">IID_IMAPIPropData</span><span class="sxs-lookup"><span data-stu-id="fe3df-115">IID_IMAPIPropData</span></span>  <br/> |
|<span data-ttu-id="fe3df-116">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="fe3df-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="fe3df-117">LPPROPDATA</span><span class="sxs-lookup"><span data-stu-id="fe3df-117">LPPROPDATA</span></span>  <br/> |
|<span data-ttu-id="fe3df-118">Modèle de transaction :</span><span class="sxs-lookup"><span data-stu-id="fe3df-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="fe3df-119">Nontransacted</span><span class="sxs-lookup"><span data-stu-id="fe3df-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fe3df-120">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="fe3df-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fe3df-121">HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="fe3df-121">HrSetObjAccess</span></span>](ipropdata-hrsetobjaccess.md) <br/> |<span data-ttu-id="fe3df-122">D�finit le niveau d'acc�s de l'objet.</span><span class="sxs-lookup"><span data-stu-id="fe3df-122">Sets the access level for the object.</span></span>  <br/> |
|[<span data-ttu-id="fe3df-123">HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="fe3df-123">HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md) <br/> |<span data-ttu-id="fe3df-124">Définit le niveau d’accès et l’état d’un ou plusieurs des propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="fe3df-124">Sets the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="fe3df-125">HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="fe3df-125">HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md) <br/> |<span data-ttu-id="fe3df-126">R�cup�re le niveau d'acc�s et l'�tat d'un ou plusieurs des propri�t�s de l'objet.</span><span class="sxs-lookup"><span data-stu-id="fe3df-126">Retrieves the access level and status for one or more of the object's properties.</span></span>  <br/> |
|[<span data-ttu-id="fe3df-127">HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="fe3df-127">HrAddObjProps</span></span>](ipropdata-hraddobjprops.md) <br/> |<span data-ttu-id="fe3df-128">Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.</span><span class="sxs-lookup"><span data-stu-id="fe3df-128">Adds one or more properties of type PT_OBJECT to the object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe3df-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe3df-129">Remarks</span></span>

<span data-ttu-id="fe3df-130">L’interface **IPropData::IMAPIProp** est implémentée par MAPI et utilisé principalement par les fournisseurs de services qui accèdent à cette implémentation en appelant la fonction [CreateIProp](createiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3df-130">The **IPropData::IMAPIProp** interface is implemented by MAPI and used primarily by service providers that access this implementation by calling the [CreateIProp](createiprop.md) function.</span></span> 
  
<span data-ttu-id="fe3df-131">Pour plus d’informations sur les niveaux d’accès sur les objets et propriétés, voir [les autorisations pour les objets et propriétés](permissions-for-mapi-objects-and-properties.md).</span><span class="sxs-lookup"><span data-stu-id="fe3df-131">For more information about access levels on objects and properties, see [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe3df-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe3df-132">See also</span></span>



[<span data-ttu-id="fe3df-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="fe3df-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

