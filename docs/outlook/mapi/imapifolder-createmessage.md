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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e740e86fc25307457119aabf6e2aa0c42a9d69b9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568223"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="6f443-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="6f443-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="6f443-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f443-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f443-105">Crée un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="6f443-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="6f443-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f443-106">Parameters</span></span>

 <span data-ttu-id="6f443-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6f443-107">_lpInterface_</span></span>
  
> <span data-ttu-id="6f443-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au nouveau message.</span><span class="sxs-lookup"><span data-stu-id="6f443-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="6f443-109">Identificateurs d’interface valides incluent IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer et IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="6f443-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="6f443-110">Passage de NULL entraîne le fournisseur de banque de messages renvoyer l’interface de message standard, [IMessage : IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="6f443-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="6f443-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6f443-111">_ulFlags_</span></span>
  
> <span data-ttu-id="6f443-112">[in] Masque de bits d’indicateurs qui contrôle la façon dont le message est créé.</span><span class="sxs-lookup"><span data-stu-id="6f443-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="6f443-113">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="6f443-113">The following flags can be set:</span></span>
    
<span data-ttu-id="6f443-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="6f443-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="6f443-115">Indique pour la banque de dossiers personnels (PST) que le message est éligible pour les règles de traitement avant que le magasin notifie n’importe quel client d’écoute de l’arrivée du nouveau message.</span><span class="sxs-lookup"><span data-stu-id="6f443-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="6f443-116">Traitement uniquement des règles s’applique aux nouveaux messages sont créés sur un serveur qui n’est pas un serveur Microsoft Exchange, car Exchange Server traite les règles pour les messages sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="6f443-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="6f443-117">Par conséquent, le fournisseur ou le client qui crée le message doit passer cet indicateur en combinaison avec l’enregistrement d’un message avec [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) à l’aide de NON_EMS_XP_SAVE, ce qui indique que le serveur n’est pas un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="6f443-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="6f443-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="6f443-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="6f443-119">Le message doit être créé doit être inclus dans le tableau contenu associé au lieu de la table des matières standard.</span><span class="sxs-lookup"><span data-stu-id="6f443-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="6f443-120">Messages associés sont masqués intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6f443-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="6f443-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6f443-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6f443-122">**CreateMessage** est autorisé à fonctionne même si l’opération de création n’est pas entièrement terminée.</span><span class="sxs-lookup"><span data-stu-id="6f443-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="6f443-123">Cela implique que le nouveau message peuvent ne pas être immédiatement disponible pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="6f443-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="6f443-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="6f443-124">_lppMessage_</span></span>
  
> <span data-ttu-id="6f443-125">[out] Pointeur vers un pointeur vers le message nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="6f443-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6f443-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6f443-126">Return value</span></span>

<span data-ttu-id="6f443-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="6f443-127">S_OK</span></span> 
  
> <span data-ttu-id="6f443-128">Le message a été créé avec succès.</span><span class="sxs-lookup"><span data-stu-id="6f443-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f443-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f443-129">Remarks</span></span>

<span data-ttu-id="6f443-130">La méthode **IMAPIFolder::CreateMessage** crée un nouveau message avec du contenu générique ou associé et affecte un identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6f443-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="6f443-131">L’identificateur d’entrée se compose d’une partie qui représente le fournisseur de banque de messages et un composant qui représente le message individuel.</span><span class="sxs-lookup"><span data-stu-id="6f443-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="6f443-132">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="6f443-132">Notes to implementers</span></span>

<span data-ttu-id="6f443-133">Vous pouvez choisir s’il faut définir toutes les propriétés de message requis dans **CreateMessage** ou dans la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du message.</span><span class="sxs-lookup"><span data-stu-id="6f443-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="6f443-134">Il est inutile de rendre ces propriétés disponible jusqu'à ce qu’une sauvegarde réussie a eu lieu.</span><span class="sxs-lookup"><span data-stu-id="6f443-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="6f443-135">Pour plus d’informations sur l’utilisation des informations associées, voir [Folder-Associated informations Tables](folder-associated-information-tables.md) et [Contenu](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6f443-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6f443-136">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="6f443-136">Notes to callers</span></span>

<span data-ttu-id="6f443-137">Certains fournisseurs de banque de message permettent l’identificateur d’entrée du message immédiatement après **CreateMessage** renvoie ; autres fournisseurs de banque de message délai sa disponibilité jusqu'à ce que le message est enregistré.</span><span class="sxs-lookup"><span data-stu-id="6f443-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="6f443-138">Étant donné que tous les fournisseurs de banque de messages génèrent un identificateur d’entrée d’un nouveau message jusqu'à ce que vous avez appelé la méthode **IMAPIProp::SaveChanges** du message, vous ne pourrez pas accéder **CreateMessage** renvoie l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6f443-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="6f443-139">En outre, le nouveau message ne peut pas être inclus dans la table des matières du dossier jusqu'à ce que l’enregistrement se produit.</span><span class="sxs-lookup"><span data-stu-id="6f443-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="6f443-140">Attendez l’identificateur d’entrée affecté vers le nouveau message à être uniques non seulement dans la banque de messages actuel, mais probablement dans toutes les banques de messages qui sont ouverts en même temps.</span><span class="sxs-lookup"><span data-stu-id="6f443-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="6f443-141">Une exception à cette règle se produit lorsque plusieurs entrées pour une banque de messages s’affichent dans le profil.</span><span class="sxs-lookup"><span data-stu-id="6f443-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="6f443-142">Ainsi, la banque de messages à ouvrir plusieurs fois et les identificateurs d’entrée à dupliquer.</span><span class="sxs-lookup"><span data-stu-id="6f443-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="6f443-143">Pour créer un message sortant, appelez la méthode de **IMAPIFolder::CreateMessage** du dossier boîte d’envoi.</span><span class="sxs-lookup"><span data-stu-id="6f443-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="6f443-144">Si vous supprimez un dossier qui contient un nouveau message avant du message est enregistré, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="6f443-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6f443-145">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6f443-145">MFCMAPI reference</span></span>

<span data-ttu-id="6f443-146">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6f443-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6f443-147">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6f443-147">**File**</span></span>|<span data-ttu-id="6f443-148">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6f443-148">**Function**</span></span>|<span data-ttu-id="6f443-149">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6f443-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6f443-150">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6f443-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="6f443-151">CFolder::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="6f443-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="6f443-152">MFCMAPI utilise la méthode **IMAPIFolder::CreateMessage** pour créer et enregistrer un nouveau message.</span><span class="sxs-lookup"><span data-stu-id="6f443-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f443-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f443-153">See also</span></span>



[<span data-ttu-id="6f443-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6f443-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="6f443-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6f443-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="6f443-156">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6f443-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

