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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412036"
---
# <a name="closeimsgsession"></a><span data-ttu-id="750b1-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="750b1-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="750b1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="750b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="750b1-105">Ferme une session de message et tous les messages créés au sein de cette session.</span><span class="sxs-lookup"><span data-stu-id="750b1-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="750b1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="750b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="750b1-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="750b1-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="750b1-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="750b1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="750b1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="750b1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="750b1-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="750b1-110">Called by:</span></span>  <br/> |<span data-ttu-id="750b1-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="750b1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="750b1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="750b1-112">Parameters</span></span>

 <span data-ttu-id="750b1-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="750b1-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="750b1-114">[in] Pointeur vers l’objet de session de message obtenu à l’aide de la fonction [OpenIMsgSession](openimsgsession.md) au début de la session de message.</span><span class="sxs-lookup"><span data-stu-id="750b1-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="750b1-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="750b1-115">Return value</span></span>

<span data-ttu-id="750b1-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="750b1-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="750b1-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="750b1-117">Remarks</span></span>

<span data-ttu-id="750b1-118">Une session de message est utilisée par les applications clientes et les fournisseurs de services qui souhaitent traiter plusieurs objets **IMessage** MAPI associés créés au-dessus des objets OLE **IStorage** sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="750b1-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="750b1-119">Le client ou le fournisseur utilise les fonctions [OpenIMsgSession](openimsgsession.md) et **CloseIMsgSession** pour encapsuler la création de tels messages dans une session de message.</span><span class="sxs-lookup"><span data-stu-id="750b1-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="750b1-120">Une fois la session de message ouverte, le client ou le fournisseur lui transmet un pointeur dans un appel à [OpenIMsgOnIStg](openimsgonistg.md) pour créer un objet **IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="750b1-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="750b1-121">Une session de message assure le suivi de tous les objets **IMessage** **-on-IStorage** ouverts pendant la durée de la session, en plus de toutes les pièces jointes et autres propriétés des messages.</span><span class="sxs-lookup"><span data-stu-id="750b1-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="750b1-122">Lorsqu’un client ou un fournisseur appelle **CloseIMsgSession,** il ferme tous ces objets.</span><span class="sxs-lookup"><span data-stu-id="750b1-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="750b1-123">L’appel de **CloseIMsgSession** est le seul moyen de fermer des objets **IMessage**-on- **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="750b1-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

