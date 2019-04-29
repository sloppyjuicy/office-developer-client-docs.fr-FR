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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422760"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="b503b-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="b503b-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="b503b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b503b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b503b-105">Renvoie un pointeur qui fournit l'accès à un objet d'administration de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b503b-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="b503b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b503b-106">Parameters</span></span>

 <span data-ttu-id="b503b-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="b503b-107">_lpUID_</span></span>
  
> <span data-ttu-id="b503b-108">dans Pointeur vers la structure [MAPIUID](mapiuid.md) qui contient l'identificateur unique pour le service de messagerie à administrer.</span><span class="sxs-lookup"><span data-stu-id="b503b-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="b503b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b503b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b503b-110">dans Toujours NULL.</span><span class="sxs-lookup"><span data-stu-id="b503b-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="b503b-111">_lppProviderAdmin_</span><span class="sxs-lookup"><span data-stu-id="b503b-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="b503b-112">remarquer Pointeur vers un pointeur vers un objet d'administration de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b503b-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b503b-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b503b-113">Return value</span></span>

<span data-ttu-id="b503b-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="b503b-114">S_OK</span></span> 
  
> <span data-ttu-id="b503b-115">L'objet d'administration du fournisseur a été renvoyé.</span><span class="sxs-lookup"><span data-stu-id="b503b-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="b503b-116">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b503b-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b503b-117">Le **MAPIUID** pointé par _lpUID_ n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="b503b-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b503b-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="b503b-118">Remarks</span></span>

<span data-ttu-id="b503b-119">La méthode **IMsgServiceAdmin:: AdminProviders** fournit l'accès à un objet d'administration de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b503b-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="b503b-120">Une administration de fournisseur est un objet qui prend en charge l'interface [IProviderAdmin](iprovideradminiunknown.md) et permet aux clients d'effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="b503b-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="b503b-121">Ajouter des fournisseurs de services à un service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b503b-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="b503b-122">Supprimer des fournisseurs de services d'un service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b503b-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="b503b-123">Ouvrez les sections de profil.</span><span class="sxs-lookup"><span data-stu-id="b503b-123">Open profile sections.</span></span>
    
- <span data-ttu-id="b503b-124">Accéder à la table du fournisseur de services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b503b-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="b503b-125">Les types de modifications qui peuvent être apportées à un service de messagerie alors que le profil est en cours d'utilisation dépendent du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b503b-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="b503b-126">Toutefois, la plupart des services de messagerie ne prennent pas en charge les modifications telles que l'ajout et la suppression de fournisseurs lorsque le profil est en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="b503b-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b503b-127">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="b503b-127">Notes to callers</span></span>

<span data-ttu-id="b503b-128">Pour récupérer la structure **MAPIUID** du service de messagerie à administrer, récupérez la colonne de propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du service de messagerie dans la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="b503b-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="b503b-129">Pour plus d'informations, reportez-vous à la procédure décrite dans la méthode [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b503b-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b503b-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b503b-130">MFCMAPI reference</span></span>

<span data-ttu-id="b503b-131">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b503b-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b503b-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="b503b-132">**File**</span></span>|<span data-ttu-id="b503b-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="b503b-133">**Function**</span></span>|<span data-ttu-id="b503b-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="b503b-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b503b-135">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="b503b-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="b503b-136">CMsgServiceTableDlg:: OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="b503b-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="b503b-137">MFCMAPI utilise la méthode **IMsgServiceAdmin:: AdminProviders** pour ouvrir un objet d'administration de fournisseur pour un service.</span><span class="sxs-lookup"><span data-stu-id="b503b-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b503b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b503b-138">See also</span></span>



[<span data-ttu-id="b503b-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b503b-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="b503b-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b503b-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b503b-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b503b-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="b503b-142">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="b503b-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

