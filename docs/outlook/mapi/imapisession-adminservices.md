---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405904"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="bb74a-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="bb74a-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="bb74a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb74a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb74a-105">Renvoie un [pointeur IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications aux services de message.</span><span class="sxs-lookup"><span data-stu-id="bb74a-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="bb74a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb74a-106">Parameters</span></span>

 <span data-ttu-id="bb74a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bb74a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bb74a-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="bb74a-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="bb74a-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="bb74a-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="bb74a-110">[out] Pointeur vers un pointeur vers un objet d’administration de service de message.</span><span class="sxs-lookup"><span data-stu-id="bb74a-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb74a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bb74a-111">Return value</span></span>

<span data-ttu-id="bb74a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb74a-112">S_OK</span></span> 
  
> <span data-ttu-id="bb74a-113">Un pointeur vers un objet d’administration de service de message a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="bb74a-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="bb74a-114">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="bb74a-114">Notes to callers</span></span>

<span data-ttu-id="bb74a-115">La **méthode IMAPISession::AdminServices** crée un objet d’administration de service de message, un objet qui prend en charge l’interface **IMsgServiceAdmin** et renvoie un pointeur.</span><span class="sxs-lookup"><span data-stu-id="bb74a-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="bb74a-116">À l’aide de ce pointeur, vous pouvez appeler des méthodes **IMsgServiceAdmin** pour modifier les services de message dans le profil de session.</span><span class="sxs-lookup"><span data-stu-id="bb74a-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="bb74a-117">N’ignorez pas que ces modifications ne prennent effet qu’après la session suivante . la session en cours n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="bb74a-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bb74a-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="bb74a-118">MFCMAPI reference</span></span>

<span data-ttu-id="bb74a-119">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bb74a-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bb74a-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="bb74a-120">**File**</span></span>|<span data-ttu-id="bb74a-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="bb74a-121">**Function**</span></span>|<span data-ttu-id="bb74a-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="bb74a-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb74a-123">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="bb74a-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="bb74a-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="bb74a-124">GetServerName</span></span>  <br/> |<span data-ttu-id="bb74a-125">MFCMAPI utilise la méthode **IMAPISession::AdminServices** pour accéder au profil afin de lire le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="bb74a-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb74a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb74a-126">See also</span></span>



[<span data-ttu-id="bb74a-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb74a-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="bb74a-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="bb74a-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="bb74a-129">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb74a-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="bb74a-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="bb74a-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

