---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411308"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a><span data-ttu-id="4e69d-103">IMAPISupport::GetSvcConfigSupportObj</span><span class="sxs-lookup"><span data-stu-id="4e69d-103">IMAPISupport::GetSvcConfigSupportObj</span></span>

  
  
<span data-ttu-id="4e69d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e69d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e69d-105">Crée un objet de prise en charge du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4e69d-105">Creates a message service support object.</span></span>
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a><span data-ttu-id="4e69d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e69d-106">Parameters</span></span>

 <span data-ttu-id="4e69d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e69d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4e69d-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="4e69d-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4e69d-109">_lppSvcSupport_</span><span class="sxs-lookup"><span data-stu-id="4e69d-109">_lppSvcSupport_</span></span>
  
> <span data-ttu-id="4e69d-110">remarquer Pointeur vers un pointeur vers le nouvel objet de prise en charge du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4e69d-110">[out] A pointer to a pointer to the new message service support object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e69d-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4e69d-111">Return value</span></span>

<span data-ttu-id="4e69d-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e69d-112">S_OK</span></span> 
  
> <span data-ttu-id="4e69d-113">L'objet de prise en charge de la configuration a été correctement créé.</span><span class="sxs-lookup"><span data-stu-id="4e69d-113">The configuration support object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e69d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e69d-114">Remarks</span></span>

<span data-ttu-id="4e69d-115">La méthode **IMAPISupport:: GetSvcConfigSupportObj** est implémentée pour tous les objets de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="4e69d-115">The **IMAPISupport::GetSvcConfigSupportObj** method is implemented for all support objects.</span></span> <span data-ttu-id="4e69d-116">Les fournisseurs de services appellent **GetSvcConfigSupportObj** pour créer un objet de prise en charge de configuration à transmettre à une fonction de point d'entrée de service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4e69d-116">Service providers call **GetSvcConfigSupportObj** to create a configuration support object to pass to a message service entry point function.</span></span> 
  
<span data-ttu-id="4e69d-117">Une fonction de point d'entrée de service de messagerie est basée sur le prototype [MSGSERVICEENTRY](msgserviceentry.md) et est appelée par les méthodes de l'interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="4e69d-117">A message service entry point function is based on the [MSGSERVICEENTRY](msgserviceentry.md) prototype and is called by methods of the [IMsgServiceAdmin](imsgserviceadminiunknown.md) interface.</span></span> <span data-ttu-id="4e69d-118">Une fonction de point d'entrée de service de messagerie permet aux services de message de se configurer eux-mêmes ou d'effectuer d'autres actions lorsque le profil est modifié.</span><span class="sxs-lookup"><span data-stu-id="4e69d-118">A message service entry point function allows message services to configure themselves or perform other actions when the profile is changed.</span></span> <span data-ttu-id="4e69d-119">Les fonctions de point d'entrée de service de messagerie peuvent prendre en charge les modifications de configuration en affichant une feuille de propriétés ou via un tableau de valeurs de propriété passé à la méthode [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4e69d-119">Message service entry point functions can support configuration changes by displaying a property sheet or through a property value array passed to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e69d-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e69d-120">See also</span></span>



[<span data-ttu-id="4e69d-121">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e69d-121">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="4e69d-122">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="4e69d-122">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="4e69d-123">IMsgServiceAdmin::CreateMsgService</span><span class="sxs-lookup"><span data-stu-id="4e69d-123">IMsgServiceAdmin::CreateMsgService</span></span>](imsgserviceadmin-createmsgservice.md)
  
[<span data-ttu-id="4e69d-124">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e69d-124">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)
  
[<span data-ttu-id="4e69d-125">MSGSERVICEENTRY</span><span class="sxs-lookup"><span data-stu-id="4e69d-125">MSGSERVICEENTRY</span></span>](msgserviceentry.md)
  
[<span data-ttu-id="4e69d-126">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e69d-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

