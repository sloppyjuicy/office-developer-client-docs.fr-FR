---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783036"
---
# <a name="closeimsgsession"></a><span data-ttu-id="7b49e-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="7b49e-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="7b49e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7b49e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7b49e-105">Ferme une session de messagerie et de tous les messages créés dans cette session.</span><span class="sxs-lookup"><span data-stu-id="7b49e-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7b49e-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7b49e-106">Header file:</span></span>  <br/> |<span data-ttu-id="7b49e-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="7b49e-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="7b49e-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="7b49e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7b49e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7b49e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7b49e-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="7b49e-110">Called by:</span></span>  <br/> |<span data-ttu-id="7b49e-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="7b49e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="7b49e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b49e-112">Parameters</span></span>

 <span data-ttu-id="7b49e-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="7b49e-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="7b49e-114">[in] Pointeur vers l’objet de la session message obtenue à l’aide de la fonction [OpenIMsgSession](openimsgsession.md) au début de la session de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7b49e-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7b49e-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7b49e-115">Return value</span></span>

<span data-ttu-id="7b49e-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7b49e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b49e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7b49e-117">Remarks</span></span>

<span data-ttu-id="7b49e-118">Une session de messagerie est utilisée par les applications clientes et des fournisseurs de services want gérer plusieurs objets MAPI **IMessage** connexes greffées sur des objets OLE **IStorage** sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="7b49e-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="7b49e-119">Le client ou le fournisseur utilise les fonctions [OpenIMsgSession](openimsgsession.md) et **CloseIMsgSession** pour encapsuler la création de ces messages à l’intérieur d’une session de messagerie.</span><span class="sxs-lookup"><span data-stu-id="7b49e-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="7b49e-120">Une fois la session de messagerie est ouvert, le client ou le fournisseur lui passe un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un nouveau **IMessage**- sur - objet **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="7b49e-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="7b49e-121">Enregistre une session de messagerie de tous les objets **IMessage**- sur - **IStorage** ouverts pendant la durée de la session, en plus de toutes les pièces jointes et d’autres propriétés des messages.</span><span class="sxs-lookup"><span data-stu-id="7b49e-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="7b49e-122">Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession**, il ferme tous ces objets.</span><span class="sxs-lookup"><span data-stu-id="7b49e-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="7b49e-123">L’appel de **CloseIMsgSession** est la seule façon de fermer **IMessage**- sur - objets **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="7b49e-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

