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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326193"
---
# <a name="openimsgsession"></a><span data-ttu-id="d321f-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="d321f-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="d321f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d321f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d321f-105">Crée et ouvre une session de message qui regroupe les messages créés dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="d321f-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d321f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="d321f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d321f-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="d321f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="d321f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="d321f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d321f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d321f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d321f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="d321f-110">Called by:</span></span>  <br/> |<span data-ttu-id="d321f-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="d321f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="d321f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d321f-112">Parameters</span></span>

 <span data-ttu-id="d321f-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="d321f-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="d321f-114">dans Pointeur vers un objet de l'allocation de mémoire qui expose [](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) l'interface OLE imalloc.</span><span class="sxs-lookup"><span data-stu-id="d321f-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="d321f-115">MAPI doit utiliser cette méthode d'allocation lorsque vous utilisez l'interface OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="d321f-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="d321f-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d321f-116">_ulFlags_</span></span>
  
> <span data-ttu-id="d321f-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="d321f-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="d321f-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="d321f-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="d321f-119">remarquer Pointeur vers un pointeur vers l'objet de session de message renvoyé.</span><span class="sxs-lookup"><span data-stu-id="d321f-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d321f-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d321f-120">Return value</span></span>

<span data-ttu-id="d321f-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d321f-121">S_OK</span></span>
  
> <span data-ttu-id="d321f-122">La session a été ouverte.</span><span class="sxs-lookup"><span data-stu-id="d321f-122">The session was opened.</span></span>
    
<span data-ttu-id="d321f-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d321f-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="d321f-124">_lpMalloc_ ou _lppMsgSess_ est null.</span><span class="sxs-lookup"><span data-stu-id="d321f-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="d321f-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="d321f-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="d321f-126">Des indicateurs non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="d321f-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="d321f-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d321f-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d321f-128">Lors de l'appel de cette fonction, un client ou un fournisseur de services définit l'indicateur MAPI_UNICODE pour créer des fichiers. MSG Unicode.</span><span class="sxs-lookup"><span data-stu-id="d321f-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="d321f-129">Le fichier [IMessage](imessageimapiprop.md) obtenu affiche STORE_UNICODE_OK dans son PR_STORE_SUPPORT_MASK et prend en charge les propriétés Unicode.</span><span class="sxs-lookup"><span data-stu-id="d321f-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d321f-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="d321f-130">Remarks</span></span>

<span data-ttu-id="d321f-131">Une session de message est utilisée par les applications clientes et les fournisseurs de services qui souhaitent traiter avec plusieurs objets de la fonction IMessage MAPI associés [: IMAPIProp](imessageimapiprop.md) objets construits sur des objets OLE **IStorage** sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="d321f-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="d321f-132">Le client ou le fournisseur utilise les fonctions **OpenIMsgSession** et [CloseIMsgSession](closeimsgsession.md) pour encapsuler la création de ces messages à l'intérieur d'une session de message.</span><span class="sxs-lookup"><span data-stu-id="d321f-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="d321f-133">Une fois la session de message ouverte, le client ou le fournisseur lui transmet un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un nouvel objet **IMessage**sur l' **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="d321f-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="d321f-134">Une session de message assure le suivi de tous les objets **IMessage**sur le **IStorage** créés pendant la durée de la session, en plus de toutes les pièces jointes et d'autres propriétés des messages.</span><span class="sxs-lookup"><span data-stu-id="d321f-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="d321f-135">Lorsqu'un client ou un fournisseur appelle **CloseIMsgSession**, il ferme tous ces objets.</span><span class="sxs-lookup"><span data-stu-id="d321f-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="d321f-136">L'appel de **CloseIMsgSession** est la seule façon de fermer des objets **IMessage**-sur- **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="d321f-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="d321f-137">**OpenIMsgSession** est utilisé par les clients et les fournisseurs qui ont besoin de pouvoir gérer plusieurs messages connexes en tant qu'objets **IStorage** OLE.</span><span class="sxs-lookup"><span data-stu-id="d321f-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="d321f-138">Si un seul de ces messages doit être ouvert à la fois, il n'est pas nécessaire de suivre plusieurs messages et aucune raison de créer une session de message avec **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="d321f-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="d321f-139">Étant donné qu'il s'agit d'un objet OLE sous-jacent, MAPI doit utiliser l'allocation de mémoire OLE.</span><span class="sxs-lookup"><span data-stu-id="d321f-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="d321f-140">Pour plus d'informations sur les objets de stockage structuré OLE et l'allocation de mémoire OLE, consultez la rubrique [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="d321f-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

