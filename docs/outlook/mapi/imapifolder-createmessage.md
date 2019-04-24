---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d38648f5e3084c8342fca8d18f0bd3efc915155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280084"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="4394d-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="4394d-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="4394d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4394d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4394d-105">Crée un message.</span><span class="sxs-lookup"><span data-stu-id="4394d-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="4394d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4394d-106">Parameters</span></span>

 <span data-ttu-id="4394d-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="4394d-107">_lpInterface_</span></span>
  
> <span data-ttu-id="4394d-108">dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4394d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="4394d-109">Les identificateurs d'interface valides sont IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="4394d-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="4394d-110">En passant la valeur NULL, le fournisseur de banque de messages renvoie l'interface de message standard, [IMessage: IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="4394d-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="4394d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4394d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="4394d-112">dans Masque de des indicateurs qui contrôle la manière dont le message est créé.</span><span class="sxs-lookup"><span data-stu-id="4394d-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="4394d-113">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="4394d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="4394d-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="4394d-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="4394d-115">Indique à la Banque de dossiers personnels (PST) que le message est éligible pour le traitement des règles avant que le magasin ne notifie à un client d'écoute la réception du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4394d-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="4394d-116">Le traitement des règles s'applique uniquement aux nouveaux messages créés sur un serveur qui n'est pas un serveur Microsoft Exchange, car Exchange Server traite les règles pour les messages sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="4394d-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="4394d-117">Par conséquent, le fournisseur ou le client qui crée le message doit transmettre cet indicateur en association avec l'enregistrement d'un message avec [IMAPIPProp:: SaveChanges](imapiprop-savechanges.md) à l'aide de NON_EMS_XP_SAVE, ce qui indique que le serveur n'est pas un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="4394d-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="4394d-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="4394d-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="4394d-119">Le message à créer doit être inclus dans la table des matières associée au lieu de la table des matières standard.</span><span class="sxs-lookup"><span data-stu-id="4394d-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="4394d-120">Les messages associés sont masqués lors de l'interaction de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4394d-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="4394d-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="4394d-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="4394d-122">**CreateMessage** est autorisé même si l'opération de création n'est pas entièrement terminée.</span><span class="sxs-lookup"><span data-stu-id="4394d-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="4394d-123">Cela signifie que le nouveau message peut ne pas être immédiatement disponible pour l'appelant.</span><span class="sxs-lookup"><span data-stu-id="4394d-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="4394d-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="4394d-124">_lppMessage_</span></span>
  
> <span data-ttu-id="4394d-125">remarquer Pointeur vers un pointeur vers le message nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="4394d-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4394d-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4394d-126">Return value</span></span>

<span data-ttu-id="4394d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="4394d-127">S_OK</span></span> 
  
> <span data-ttu-id="4394d-128">Le message a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="4394d-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4394d-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="4394d-129">Remarks</span></span>

<span data-ttu-id="4394d-130">La méthode **IMAPIFolder:: CreateMessage** crée un nouveau message avec un contenu générique ou associé et assigne un identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="4394d-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="4394d-131">L'identificateur d'entrée se compose d'un composant qui représente le fournisseur de banque de messages et d'un composant qui représente le message individuel.</span><span class="sxs-lookup"><span data-stu-id="4394d-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4394d-132">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="4394d-132">Notes to implementers</span></span>

<span data-ttu-id="4394d-133">Vous pouvez choisir de définir toutes les propriétés de message requises dans **CreateMessage** ou dans la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) du message.</span><span class="sxs-lookup"><span data-stu-id="4394d-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="4394d-134">Vous n'avez pas besoin de mettre ces propriétés à disposition tant qu'un enregistrement réussi n'a pas été effectué.</span><span class="sxs-lookup"><span data-stu-id="4394d-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="4394d-135">Pour plus d'informations sur l'utilisation des informations associées, consultez la rubrique tables d' [informations associées aux dossiers](folder-associated-information-tables.md) et [tables des matières](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4394d-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4394d-136">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="4394d-136">Notes to callers</span></span>

<span data-ttu-id="4394d-137">Certains fournisseurs de banques de messages permettent à l'identificateur d'entrée du nouveau message d'être disponible immédiatement après que la méthode **CreateMessage** a été renvoyée; les autres fournisseurs de banques de messages retardent leur disponibilité jusqu'à ce que le message soit enregistré.</span><span class="sxs-lookup"><span data-stu-id="4394d-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="4394d-138">Étant donné que tous les fournisseurs de banques de messages ne génèrent pas d'identificateur d'entrée pour un nouveau message tant que vous n'avez pas appelé la méthode **IMAPIProp:: SaveChanges** du message, il se peut que vous ne puissiez pas accéder à l'identificateur d'entrée lorsque **CreateMessage** renvoie.</span><span class="sxs-lookup"><span data-stu-id="4394d-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="4394d-139">Par ailleurs, il se peut que le nouveau message ne soit pas inclus dans la table des matières du dossier tant que l'enregistrement n'a pas lieu.</span><span class="sxs-lookup"><span data-stu-id="4394d-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="4394d-140">Attendez-vous à ce que l'identificateur d'entrée attribué au nouveau message soit unique non seulement dans la Banque de messages actuelle, mais probablement dans toutes les banques de messages ouvertes en même temps.</span><span class="sxs-lookup"><span data-stu-id="4394d-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="4394d-141">Une exception à cette règle se produit lorsque plusieurs entrées pour une banque de messages apparaissent dans le profil.</span><span class="sxs-lookup"><span data-stu-id="4394d-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="4394d-142">Ainsi, la Banque de messages est ouverte plusieurs fois et les identificateurs d'entrée doivent être dupliqués.</span><span class="sxs-lookup"><span data-stu-id="4394d-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="4394d-143">Pour créer un message sortant, appelez la méthode **IMAPIFolder:: CreateMessage** du dossier boîte d'envoi.</span><span class="sxs-lookup"><span data-stu-id="4394d-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="4394d-144">Si vous supprimez un dossier qui contient un nouveau message avant que le message ne soit enregistré, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="4394d-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4394d-145">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4394d-145">MFCMAPI reference</span></span>

<span data-ttu-id="4394d-146">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4394d-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4394d-147">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="4394d-147">**File**</span></span>|<span data-ttu-id="4394d-148">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="4394d-148">**Function**</span></span>|<span data-ttu-id="4394d-149">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="4394d-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4394d-150">FolderDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="4394d-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="4394d-151">CFolder:: OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="4394d-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="4394d-152">MFCMAPI utilise la méthode **IMAPIFolder:: CreateMessage** pour créer et enregistrer un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="4394d-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4394d-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4394d-153">See also</span></span>



[<span data-ttu-id="4394d-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="4394d-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="4394d-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="4394d-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="4394d-156">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4394d-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

