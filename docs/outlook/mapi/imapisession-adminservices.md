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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783948"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="f2918-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="f2918-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="f2918-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f2918-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f2918-105">Retourne un pointeur [IMsgServiceAdmin](imsgserviceadminiunknown.md) pour apporter des modifications à des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="f2918-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="f2918-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="f2918-106">Parameters</span></span>

 <span data-ttu-id="f2918-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f2918-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f2918-108">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="f2918-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f2918-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="f2918-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="f2918-110">[out] Pointeur vers un pointeur vers un objet de l’administration de service de message.</span><span class="sxs-lookup"><span data-stu-id="f2918-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2918-111">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f2918-111">Return value</span></span>

<span data-ttu-id="f2918-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2918-112">S_OK</span></span> 
  
> <span data-ttu-id="f2918-113">Un pointeur vers un objet d’administration service message a été renvoyé avec succès.</span><span class="sxs-lookup"><span data-stu-id="f2918-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="f2918-114">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="f2918-114">Notes to callers</span></span>

<span data-ttu-id="f2918-115">La méthode **IMAPISession::AdminServices** crée un objet d’administration service message, un objet qui prend en charge l’interface **IMsgServiceAdmin** et retourne un pointeur.</span><span class="sxs-lookup"><span data-stu-id="f2918-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="f2918-116">À l’aide de ce pointeur, vous pouvez appeler des méthodes de **IMsgServiceAdmin** pour modifier les services de messagerie dans le profil de la session.</span><span class="sxs-lookup"><span data-stu-id="f2918-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="f2918-117">Sachez que ces modifications ne prendront effet jusqu'à la prochaine session ; la session en cours n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="f2918-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f2918-118">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f2918-118">MFCMAPI reference</span></span>

<span data-ttu-id="f2918-119">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f2918-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f2918-120">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f2918-120">**File**</span></span>|<span data-ttu-id="f2918-121">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f2918-121">**Function**</span></span>|<span data-ttu-id="f2918-122">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f2918-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f2918-123">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f2918-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f2918-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="f2918-124">GetServerName</span></span>  <br/> |<span data-ttu-id="f2918-125">MFCMAPI utilise la méthode **IMAPISession::AdminServices** pour accéder au profil pour lire le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="f2918-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2918-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2918-126">See also</span></span>



[<span data-ttu-id="f2918-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2918-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="f2918-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="f2918-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="f2918-129">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2918-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f2918-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f2918-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

