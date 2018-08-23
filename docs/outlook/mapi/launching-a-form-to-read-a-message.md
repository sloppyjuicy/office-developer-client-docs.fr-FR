---
title: Lancement d’un formulaire pour lire un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 54a4b805-2ab7-4fb7-b0ea-4a33ead27451
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b9166090321aa24e35fe1c82908aec0c403095cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593738"
---
# <a name="launching-a-form-to-read-a-message"></a><span data-ttu-id="9594e-103">Lancement d’un formulaire pour lire un message</span><span class="sxs-lookup"><span data-stu-id="9594e-103">Launching a Form to Read a Message</span></span>

  
  
<span data-ttu-id="9594e-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9594e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9594e-105">L’implémentation de formulaire serveur doit attendre la séquence suivante d’appels de méthode à leur serveur du formulaire et les objets de formulaire lorsqu’une application cliente charge un message :</span><span class="sxs-lookup"><span data-stu-id="9594e-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application loads a message:</span></span>
  
1. <span data-ttu-id="9594e-106">L’application cliente ouvre le Gestionnaire de formulaire avec un appel à la fonction [MAPIOpenFormMgr](mapiopenformmgr.md) .</span><span class="sxs-lookup"><span data-stu-id="9594e-106">The client application opens the form manager with a call to the [MAPIOpenFormMgr](mapiopenformmgr.md) function.</span></span> 
    
2. <span data-ttu-id="9594e-107">L’application cliente appelle la méthode [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) , qui renvoie un objet avec [IMAPIForm](imapiformiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="9594e-107">The client application calls the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method, which returns an object with [IMAPIForm](imapiformiunknown.md).</span></span> <span data-ttu-id="9594e-108">Le Gestionnaire de formulaire peut-être être annulée maintenant s’il ne doit pas être utilisé pour des activations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="9594e-108">The form manager may be released now if it will not be used for further form activations.</span></span> <span data-ttu-id="9594e-109">Notez qu’un appel à **LoadForm** peut prendre du temps car le Gestionnaire de formulaire peut-être installer des fichiers exécutables du serveur de formulaire avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="9594e-109">Note that a call to **LoadForm** may take some time because the form manager may have to install the form server's executable files before proceeding.</span></span> 
    
3. <span data-ttu-id="9594e-110">Le cas échéant, l’application cliente peut préparer [IMAPIViewContext](imapiviewcontextiunknown.md) opérations de contrôle qui peuvent entraîner l’objet de formulaire pour charger le message précédent ou suivant dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="9594e-110">Optionally, the client application can prepare [IMAPIViewContext](imapiviewcontextiunknown.md) to control operations that may cause the form object to load the previous or next message in the folder.</span></span> <span data-ttu-id="9594e-111">L’application cliente peut utiliser la méthode [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) pour modifier le contexte d’affichage par défaut qui a été défini lors de l’appel **LoadForm** .</span><span class="sxs-lookup"><span data-stu-id="9594e-111">The client application can use the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method to change the default view context that was set in the **LoadForm** call.</span></span> 
    
4. <span data-ttu-id="9594e-112">L’application cliente appelle la méthode [IPersistMessage::Load](ipersistmessage-load.md) pour charger les données de message dans l’objet form.</span><span class="sxs-lookup"><span data-stu-id="9594e-112">The client application calls the [IPersistMessage::Load](ipersistmessage-load.md) method to load message data into the form object.</span></span> 
    
5. <span data-ttu-id="9594e-113">L’application cliente appelle [IMAPIForm::DoVerb](imapiform-doverb.md) pour appeler le verbe open, en passant le pointeur d’interface [IMAPIViewContext](imapiviewcontextiunknown.md) facultatif.</span><span class="sxs-lookup"><span data-stu-id="9594e-113">The client application calls [IMAPIForm::DoVerb](imapiform-doverb.md) to invoke the open verb, passing the optional [IMAPIViewContext](imapiviewcontextiunknown.md) interface pointer.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9594e-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9594e-114">See also</span></span>



[<span data-ttu-id="9594e-115">Interactions avec le serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="9594e-115">Form Server Interactions</span></span>](form-server-interactions.md)

