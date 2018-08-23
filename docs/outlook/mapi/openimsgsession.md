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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 39dd053b2896ebcfcdec97d976af3e75e19f8c0b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564954"
---
# <a name="openimsgsession"></a><span data-ttu-id="41de1-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="41de1-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="41de1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41de1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41de1-105">Crée et ouvre une session de messagerie qui regroupe les messages créés qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="41de1-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41de1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="41de1-106">Header file:</span></span>  <br/> |<span data-ttu-id="41de1-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="41de1-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="41de1-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="41de1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="41de1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="41de1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="41de1-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="41de1-110">Called by:</span></span>  <br/> |<span data-ttu-id="41de1-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="41de1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="41de1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41de1-112">Parameters</span></span>

 <span data-ttu-id="41de1-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="41de1-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="41de1-114">[in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE [IMalloc](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="41de1-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="41de1-115">MAPI doit utiliser cette méthode de répartition lorsque vous travaillez avec l’interface OLE [IStorage](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="41de1-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="41de1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="41de1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="41de1-117">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="41de1-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="41de1-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="41de1-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="41de1-119">[out] Pointeur vers un pointeur vers l’objet de session message renvoyé.</span><span class="sxs-lookup"><span data-stu-id="41de1-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41de1-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="41de1-120">Return value</span></span>

<span data-ttu-id="41de1-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="41de1-121">S_OK</span></span>
  
> <span data-ttu-id="41de1-122">La session a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="41de1-122">The session was opened.</span></span>
    
<span data-ttu-id="41de1-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="41de1-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="41de1-124">_lpMalloc_ ou _lppMsgSess_ est NULL.</span><span class="sxs-lookup"><span data-stu-id="41de1-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="41de1-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="41de1-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="41de1-126">Indicateurs non valides ont été transmis.</span><span class="sxs-lookup"><span data-stu-id="41de1-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="41de1-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="41de1-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="41de1-128">Lorsque vous appelez cette fonction, un client ou fournisseur de services définit l’indicateur MAPI_UNICODE pour créer les fichiers .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="41de1-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="41de1-129">Le fichier [Imessage](imessageimapiprop.md) affiche STORE_UNICODE_OK dans son PR_STORE_SUPPORT_MASK et prend en charge les propriétés Unicode.</span><span class="sxs-lookup"><span data-stu-id="41de1-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="41de1-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="41de1-130">Remarks</span></span>

<span data-ttu-id="41de1-131">Une session de messagerie est utilisée par les applications clientes et fournisseurs de services pour gérer les problèmes liés à plusieurs concernant MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objets greffées sur des objets OLE **IStorage** sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="41de1-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="41de1-132">Le client ou le fournisseur utilise les fonctions **OpenIMsgSession** et [CloseIMsgSession](closeimsgsession.md) pour encapsuler la création de ces messages à l’intérieur d’une session de messagerie.</span><span class="sxs-lookup"><span data-stu-id="41de1-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="41de1-133">Une fois la session de messagerie est ouvert, le client ou le fournisseur lui passe un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un nouveau **IMessage**- sur - objet **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="41de1-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="41de1-134">Enregistre une session de messagerie de tous les **IMessage**- sur - objets **IStorage** créés pendant la durée de la session, en plus de toutes les pièces jointes et d’autres propriétés des messages.</span><span class="sxs-lookup"><span data-stu-id="41de1-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="41de1-135">Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession**, il ferme tous ces objets.</span><span class="sxs-lookup"><span data-stu-id="41de1-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="41de1-136">L’appel de **CloseIMsgSession** est la seule façon de fermer **IMessage**- sur - objets **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="41de1-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="41de1-137">**OpenIMsgSession** est utilisé par les clients et les fournisseurs qui requièrent la possibilité de gérer plusieurs messages connexes en tant qu’objets OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="41de1-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="41de1-138">Si seule un des messages doit être ouvert à la fois, il n’est pas nécessaire pour effectuer le suivi de plusieurs messages et aucune raison de créer une session de messagerie avec **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="41de1-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="41de1-139">Car elle porte sur un objet OLE sous-jacent, MAPI doit utiliser l’allocation de mémoire OLE.</span><span class="sxs-lookup"><span data-stu-id="41de1-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="41de1-140">Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, consultez [OLE et transfert de données](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="41de1-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

