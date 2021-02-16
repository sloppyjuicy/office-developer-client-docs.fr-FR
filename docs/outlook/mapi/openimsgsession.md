---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326193"
---
# <a name="openimsgsession"></a><span data-ttu-id="16865-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="16865-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="16865-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16865-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16865-105">Crée et ouvre une session de message qui groupe les messages créés au sein de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="16865-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16865-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="16865-106">Header file:</span></span>  <br/> |<span data-ttu-id="16865-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="16865-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="16865-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="16865-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="16865-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="16865-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="16865-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="16865-110">Called by:</span></span>  <br/> |<span data-ttu-id="16865-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="16865-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="16865-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16865-112">Parameters</span></span>

 <span data-ttu-id="16865-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="16865-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="16865-114">[in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE [IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)</span><span class="sxs-lookup"><span data-stu-id="16865-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="16865-115">MAPI doit utiliser cette méthode d’allocation lors de l’utilisation de l’interface OLE [IStorage.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage)</span><span class="sxs-lookup"><span data-stu-id="16865-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="16865-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="16865-116">_ulFlags_</span></span>
  
> <span data-ttu-id="16865-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="16865-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="16865-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="16865-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="16865-119">[out] Pointeur vers un pointeur vers l’objet de session de message renvoyé.</span><span class="sxs-lookup"><span data-stu-id="16865-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="16865-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="16865-120">Return value</span></span>

<span data-ttu-id="16865-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="16865-121">S_OK</span></span>
  
> <span data-ttu-id="16865-122">La session a été ouverte.</span><span class="sxs-lookup"><span data-stu-id="16865-122">The session was opened.</span></span>
    
<span data-ttu-id="16865-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="16865-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="16865-124">_lpMalloc_ ou  _lppMsgSess_ est NULL.</span><span class="sxs-lookup"><span data-stu-id="16865-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="16865-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="16865-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="16865-126">Des indicateurs non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="16865-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="16865-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="16865-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="16865-128">Lorsque vous appelez cette fonction, un client ou un fournisseur de services définit l MAPI_UNICODE pour créer des fichiers .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="16865-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="16865-129">Le fichier [Imessage](imessageimapiprop.md) qui en résulte affiche STORE_UNICODE_OK sa PR_STORE_SUPPORT_MASK et prend en charge les propriétés Unicode.</span><span class="sxs-lookup"><span data-stu-id="16865-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="16865-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="16865-130">Remarks</span></span>

<span data-ttu-id="16865-131">Une session de message est utilisée par les applications clientes et les fournisseurs de services qui souhaitent traiter plusieurs objets [MAPI IMessage : IMAPIProp](imessageimapiprop.md) créés au-dessus des objets OLE **IStorage** sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="16865-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="16865-132">Le client ou le fournisseur utilise les fonctions **OpenIMsgSession** et [CloseIMsgSession](closeimsgsession.md) pour encapsuler la création de tels messages dans une session de message.</span><span class="sxs-lookup"><span data-stu-id="16865-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="16865-133">Une fois la session de message ouverte, le client ou le fournisseur lui transmet un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un objet **IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="16865-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="16865-134">Une session de message assure le suivi de tous les objets **IMessage**-on- **IStorage** créés pendant la durée de la session, en plus de toutes les pièces jointes et autres propriétés des messages.</span><span class="sxs-lookup"><span data-stu-id="16865-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="16865-135">Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession,** il ferme tous ces objets.</span><span class="sxs-lookup"><span data-stu-id="16865-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="16865-136">L’appel de **CloseIMsgSession** est le seul moyen de fermer des objets **IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="16865-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="16865-137">**OpenIMsgSession** est utilisé par les clients et les fournisseurs qui nécessitent la possibilité de gérer plusieurs messages associés en tant qu’objets **OLE IStorage.**</span><span class="sxs-lookup"><span data-stu-id="16865-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="16865-138">Si un seul de ces messages doit être ouvert à la fois, il n’est pas nécessaire de suivre plusieurs messages et il n’y a aucune raison de créer une session de message avec **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="16865-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="16865-139">Étant donné qu’il traite un objet OLE sous-jacent, MAPI doit utiliser l’allocation de mémoire OLE.</span><span class="sxs-lookup"><span data-stu-id="16865-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="16865-140">Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, voir [OLE et Transfert de données.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="16865-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

