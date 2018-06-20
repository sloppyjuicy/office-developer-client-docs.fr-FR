---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9b65c8e32580fa85302b874bd17c1829ad67fd63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784220"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="394bf-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="394bf-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="394bf-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="394bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="394bf-105">Renvoie un pointeur qui fournit l’accès à un objet de l’administration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="394bf-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="394bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="394bf-106">Parameters</span></span>

 <span data-ttu-id="394bf-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="394bf-107">_lpUID_</span></span>
  
> <span data-ttu-id="394bf-108">[in] Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l’identificateur unique pour le service de message seront administrés.</span><span class="sxs-lookup"><span data-stu-id="394bf-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="394bf-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="394bf-109">_ulFlags_</span></span>
  
> <span data-ttu-id="394bf-110">[in] Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="394bf-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="394bf-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="394bf-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="394bf-112">[out] Pointeur vers un pointeur vers un objet d’administration de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="394bf-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="394bf-113">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="394bf-113">Return value</span></span>

<span data-ttu-id="394bf-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="394bf-114">S_OK</span></span> 
  
> <span data-ttu-id="394bf-115">L’objet de l’administration du fournisseur a été renvoyée avec succès.</span><span class="sxs-lookup"><span data-stu-id="394bf-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="394bf-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="394bf-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="394bf-117">Le **MAPIUID** désignés par _lpUID_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="394bf-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="394bf-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="394bf-118">Remarks</span></span>

<span data-ttu-id="394bf-119">La méthode **IMsgServiceAdmin::AdminProviders** permet d’accéder à un objet de l’administration du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="394bf-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="394bf-120">Administration du fournisseur est un objet qui prend en charge l’interface [IProviderAdmin](iprovideradminiunknown.md) et permet aux clients d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="394bf-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="394bf-121">Ajouter des fournisseurs de services à un service de message.</span><span class="sxs-lookup"><span data-stu-id="394bf-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="394bf-122">Supprimer les fournisseurs de services à partir d’un service de message.</span><span class="sxs-lookup"><span data-stu-id="394bf-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="394bf-123">Ouvrez les sections du profil.</span><span class="sxs-lookup"><span data-stu-id="394bf-123">Open profile sections.</span></span>
    
- <span data-ttu-id="394bf-124">Accéder à la table de fournisseur de service de message.</span><span class="sxs-lookup"><span data-stu-id="394bf-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="394bf-125">Les types de modifications pouvant être effectuées en réalité à un service de message alors que le profil est en cours d’utilisation dépendant du service de message.</span><span class="sxs-lookup"><span data-stu-id="394bf-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="394bf-126">Toutefois, la plupart des services de messagerie n’acceptent pas les modifications telles que l’ajout et suppression de fournisseurs alors que le profil est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="394bf-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="394bf-127">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="394bf-127">Notes to callers</span></span>

<span data-ttu-id="394bf-128">Pour récupérer la structure **MAPIUID** pour le service de message administrer, récupérez la colonne de la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de message dans la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="394bf-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="394bf-129">Pour plus d’informations, voir la procédure décrite dans la méthode [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="394bf-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="394bf-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="394bf-130">MFCMAPI reference</span></span>

<span data-ttu-id="394bf-131">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="394bf-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="394bf-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="394bf-132">**File**</span></span>|<span data-ttu-id="394bf-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="394bf-133">**Function**</span></span>|<span data-ttu-id="394bf-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="394bf-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="394bf-135">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="394bf-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="394bf-136">CMsgServiceTableDlg::OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="394bf-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="394bf-137">MFCMAPI utilise la méthode **IMsgServiceAdmin::AdminProviders** pour ouvrir un objet d’administration de fournisseur d’un service.</span><span class="sxs-lookup"><span data-stu-id="394bf-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="394bf-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="394bf-138">See also</span></span>



[<span data-ttu-id="394bf-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="394bf-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="394bf-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="394bf-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="394bf-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="394bf-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="394bf-142">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="394bf-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

